# Answer: Final Exercise

this is the answer for the final exercise. You can copy+paste into your
environment to make it run correctly.

```python

#---------------Enter Your Code Here---------------------#

model = Sequential()
# Adds the input layer and 5 neuron hidden layer
model.add(Dense(5,input_dim=2, activation='relu'))
# Adds an additional 5 neuron hidden layer
model.add(Dense(5, activation = 'relu'))
# Adds a one neuron output layer
model.add(Dense(1, activation='sigmoid'))
model.compile(loss='binary_crossentropy', optimizer='adam', metrics=['accuracy'])
model.fit(X_2D, y_mean, epochs=100, batch_size=10)
loss, _ = model.evaluate(X_2D, y_mean)
probabilities = model.predict(X_2D)
predictions = [float(np.round(x)) for x in probabilities]
accuracy = np.mean(predictions == y_mean)
print("\nLoss: %.2f, Accuracy: %.2f%%" % (loss, accuracy*100))

#--------------------------------------------------------#
```
