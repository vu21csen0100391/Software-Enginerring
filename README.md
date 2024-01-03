class WeatherModel:
  def __init__(self, a, b, c):
      self.coefficients = {'a': a, 'b': b, 'c': c}

  def temperature_at_time(self, t):
      return self.coefficients['a'] * t**2 + self.coefficients['b'] * t + self.coefficients['c']

# Instantiating the WeatherModel class with coefficients
model = WeatherModel(a=1, b=2, c=3)

# Example time point
time_point = 5
temperature = model.temperature_at_time(time_point)
print(f"Temperature at time {time_point} is {temperature}")

# Calculating temperatures for multiple time points
time_points = [0, 1, 2, 3, 4, 5]
for t in time_points:
  temperature = model.temperature_at_time(t)
  print(f"Temperature at time {t} is {temperature}")
