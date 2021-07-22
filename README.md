from cryptography.fernet inport Fernet


def write_key()
    key = fernet.generate_key()
    with open("key.key", "wb") as key_file:
      key_file.wirte(key)'''

def load_key():
   file = open("key.key", "rb").read()
   key = file.read()
   file.close()
   return key

key = load_key() 
fer = Fernet(key)

def view():
     with open('passwords.txt', 'r') as f:
        for line in r.readlines():
          date =line.rstrip()
          user, passw = date.split("|")
          print("User:", user, ", Password:", fer.decrypt(passw.encode()).decode())


def add():
    name == input('Account Name: ')
    Pwd = input("Password: ")
    
    with open('passwords.txt', 'a') as f:
        f.write(name + "|" + fer.encrypt(pwd.encode()).decode() + "\n")
while True: 
    mode  =input("Would you like to add a new password or veiw existing one (view, add), press q to quit? ").lower()
    if mode == "q":
        break
        
    if mode == "view"
      view()
    elif mode == "add":
      add()
    else:
      print("Invaild mode.")
      contiue
