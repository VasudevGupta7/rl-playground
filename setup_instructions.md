#  System Setup

## Openai gym
Inorder to install openai gym, run the following command in mac terminal:
- `pip install gym`

Run the below command in order to use atari environments:
- `pip install gym[atari]` 

## ViZDoom
Inorder to install ViZDoom, run following commands in mac terminal (1st two commands were for installing dependencies for installing ViZDoom):
- `brew install cmake boost sdl2 wget`
- `brew cask install julia`
- `pip install vizdoom`

## Setup- Google Colab
Inorder to render env in colab, we need to need to install some dependencies; so run following commands in colab:
- `!apt-get install python-opengl -y`
- `!apt install xvfb -y`
- `!pip install pyvirtualdisplay`
- `!pip install piglet`
- `!apt-get install x11-utils`

After that run the following code once:
- `from pyvirtualdisplay import Display`
- `from IPython import display`
- `Display().start()`

Then put the following command, just before the episode starts (need to run only once):
- `img = plt.imshow(env.render('rgb_array'))`

Then put the following code, where we generally put `env.render()`:
- `img.set_data(env.render('rgb_array'))` # just update the data
- `display.display(plt.gcf())`
- `display.clear_output(wait=True)`



