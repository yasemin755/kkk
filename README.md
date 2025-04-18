# kkk
inputText = 'secret message'
key = 5
mode = 'decrypt'
ledger = 'abcdehıklhlıggujfvjbhu 1234567890'
outputText = ''
for char in inputText:
    inputIndex = ledger.find(char)
    if mode == 'encrpt':
        outputIndex = inputIndex + key
    elif mode =='decrypt':
        outputIndex = inputIndex - key
    if inputIndex >= len(ledger):
        outputIndex = outputIndex - len(ledger)
    elif outputIndex < 0:
        outputIndex = outputIndex + len(ledger)
    outputText =outputText + ledger[outputIndex]
print(outputText)
