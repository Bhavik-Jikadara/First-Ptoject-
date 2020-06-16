# simple project :
import os, shutil

user_info = { 
    'audio_extension' : ('.mp3','.m4a','.wav','.fac'),
    'videos_extention' : ('.mp4',".mkv",'.flv','.mpeg','.avi'),
    'document_extention' : ('.doc','.pdf','.txt'),
    'python_extension' : ('.py')
}

folder_path = input("enter the folder path :")

def folder_finder(folder_path,file_exetensions):
    files = []
    for file in os.listdir(folder_path):
        for extension in file_exetensions:
            if file.endswith(extension):
                files.append(file)
    return files

# print(folder_finder(folder_path,audio_extension))

for extension_type, extension_tuple in user_info.items():
    folder_name = extension_type.split('_')[0] + 'Flies'
    folders_path = os.path.join(folder_path, folder_name)
    os.mkdir(folders_path)
    for item in folder_finder(folder_path,extension_tuple):
        item_path = os.path.join(folder_path,item)
        item_new_path = os.path.join(folders_path,item)
        shutil.move(item_path,item_new_path)
