# project_gutenberg_character_generation

1. keep the number of memory units the same at 256, but add a second layer.
model = Sequential()
model.add(LSTM(256, input_shape=(X.shape[1], X.shape[2]), return_sequences=True))
model.add(Dropout(0.2))
model.add(LSTM(256))
model.add(Dropout(0.2))
model.add(Dense(y.shape[1], activation='softmax'))
model.compile(loss='categorical_crossentropy', optimizer='adam')

2. Set batch_size = 32

3. Increase the number of training epochs from 20 to 50 or 100
