



import configparser

config = configparser.ConfigParser()
config.read("C:\\Users\lc\.spyder-py3\config\spyder.ini")
config.sections()

[option for option in config['help']]

##########################
### Create Dictionaru ###
#########################
parser = configparser.ConfigParser()
parser.read_dict(
    {'section1': 
        {'tag1': '1','tag2': '2','tag3': '3'},
    'section2': 
        {'tagA': 'A','tagB': 'B','tagC': 'C'},
    'section3': 
        {'foo': 'x','bar': 'y','baz': 'z'} })
parser.sections()  #['section1', 'section2', 'section3']
[option for option in parser['section3']] # ['foo', 'bar', 'baz']



##############################
### Read Text/String file ###
#############################
sample_config = """
[My Settings]
user = username
profile = /my/directory/to/profile.png
gender = male
[My new Settings]
user = jamal.hosein.shah
profile = /my/directory/to/profile.png
gender = male

"""
# creates an instance of ConfigParser called config 
config = configparser.ConfigParser()  

#read the instance of string using read_string() method
config.read_string(sample_config)

config.sections()  #['My Settings']
user = config["My new Settings"]["user"]  #'username'
user


######################################## OUTPUT ##################################################################

Out[1]: 
['main',
 'internal_console',
 'main_interpreter',
 'ipython_console',
 'variable_explorer',
 'plots',
 'editor',
 'historylog',
 'help',
 'onlinehelp',
 'outline_explorer',
 'project_explorer',
 'explorer',
 'find_in_files',
 'breakpoints',
 'profiler',
 'pylint',
 'workingdir',
 'shortcuts',
 'appearance',
 'lsp-server',
 'fallback-completions',
 'snippet-completions',
 'kite',
 'run']

[option for option in config['help']]
Out[2]: 
['enable',
 'max_history_entries',
 'wrap',
 'connect/editor',
 'connect/ipython_console',
 'math',
 'automatic_import',
 'rich_mode',
 'first_time']

parser = configparser.ConfigParser()
parser.read_dict(
    {'section1': 
        {'tag1': '1','tag2': '2','tag3': '3'},
    'section2': 
        {'tagA': 'A','tagB': 'B','tagC': 'C'},
    'section3': 
        {'foo': 'x','bar': 'y','baz': 'z'} })
parser.sections()  #['section1', 'section2', 'section3']
[option for option in parser['section3']]
Out[3]: ['foo', 'bar', 'baz']


sample_config = """
[My Settings]
user = username
profile = /my/directory/to/profile.png
gender = male
[My new Settings]
user = jamal.hosein.shah
profile = /my/directory/to/profile.png
gender = male

"""
# creates an instance of ConfigParser called config 
config = configparser.ConfigParser()  

#read the instance of string using read_string() method
config.read_string(sample_config)


 ['My Settings', 'My new Settings']
 
 'jamal.hosein.shah'
 
 
