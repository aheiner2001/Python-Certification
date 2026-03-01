** start of main.py **

def add_setting(dictionary, key_value):
    key = key_value[0].lower()
    value = key_value[1].lower()
    
    if key in dictionary:
        return(f"Setting '{key}' already exists! Cannot add a new setting with this name.")
    else:
        dictionary[key] = value
        return (f"Setting '{key}' added with value '{value}' successfully!")


def update_setting(dictionary, key_value):
    key = key_value[0].lower()
    value = key_value[1].lower()

    if key in dictionary:
        dictionary[key] = value
        return (f"Setting '{key}' updated to '{value}' successfully!")
    else:
        return (f"Setting '{key}' does not exist! Cannot update a non-existing setting.")

def delete_setting(dictionary, key_value):
    key = key_value.lower()
    if key in dictionary:
        dictionary.pop(key, None)
        return (f"Setting '{key}' deleted successfully!")
    else:
        return ("Setting not found!")

def view_settings(dictionary):
    if not dictionary:
        return("No settings available.")
    
    formated = 'Current User Settings:\n'
    for key, value in dictionary.items():
        key = key.capitalize()
        formated += f"{key}: {value}\n"
    return formated
    


test_settings = {
    'them': 'snobby'
}

view_settings({'theme': 'dark', 'notifications': 'enabled', 'volume': 'high'}) 


# Current User Settings:
# Theme: dark
# Notifications: enabled
# Volume: high

** end of main.py **

