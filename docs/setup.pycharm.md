
#Debugging Jupyter in Pycharm
##Jupyter command `jupyter-notebook` not found.
- configure jupyter server> lab --no-browser --allow-root --port=52959 --ip=0.0.0.0

##could not collect to some 127.0.0.1:random seeming port
- stop all interpreter-run-id containers
- configure jupyter server> lab --no-browser --allow-root --port=<random seeming port> --ip=0.0.0.0