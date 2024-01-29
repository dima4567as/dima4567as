from scipy.stats import binom

n = 260
p = 0.94

# Знаходження ймовірностей для різних k
probabilities = [binom.pmf(k, n, p) for k in range(n+1)]

# Знаходження найбільш ймовірного k
most_probable_k = probabilities.index(max(probabilities))

print("Найімовірніше число ящиків з цілими банками:", most_probable_k)
print("Ймовірність:", max(probabilities))
