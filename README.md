# # import necessary modules
#
# # for implementing the HTTP Web servers
# import http.server
#
# # provides access to the BSD socket interface
# import socket
#
# # a framework for network servers
# import socketserver
#
# # to display a Web-based documents to users
# import webbrowser
#
# # to generate qrcode
# import pyqrcode
# from pyqrcode import QRCode
#
# # convert into png format
# import png
#
# # to access operating system control
# import os
#
#
# # assigning the appropriate port value
# PORT = 8010
# # this finds the name of the computer user
# os.environ['USERPROFILE']
#
#
# # changing the directory to access the files desktop
# # with the help of os module
# desktop = os.path.join(os.path.join(os.environ['USERPROFILE']),
# 					'OneDrive')
# os.chdir(desktop)
#
#
# # creating a http request
# Handler = http.server.SimpleHTTPRequestHandler
# # returns, host name of the system under
# # which Python interpreter is executed
# hostname = socket.gethostname()
#
#
# # finding the IP address of the PC
# s = socket.socket(socket.AF_INET, socket.SOCK_DGRAM)
# s.connect(("8.8.8.8", 80))
# IP = "http://" + s.getsockname()[0] + ":" + str(PORT)
# link = IP
#
#
# # converting the IP address into the form of a QRcode
# # with the help of pyqrcode module
#
# # converts the IP address into a Qrcode
# url = pyqrcode.create(link)
# # saves the Qrcode inform of svg
# url.svg("myqr.svg", scale=8)
# # opens the Qrcode image in the web browser
# webbrowser.open('myqr.svg')
#
#
# # Creating the HTTP request and serving the
# # folder in the PORT 8010,and the pyqrcode is generated
#
# # continuous stream of data between client and server
# with socketserver.TCPServer(("", PORT), Handler) as httpd:
# 	print("serving at port", PORT)
# 	print("Type this in your Browser", IP)
# 	print("or Use the QRCode")
# 	httpd.serve_forever()



# import necessary modules
# import http.server
# import socket
# import socketserver
# import webbrowser
# import pyqrcode
# import os
#
# # for tkinter GUI
# import tkinter as tk
# from tkinter import messagebox
#
# # setting up the port
# PORT = 8010
#
# # getting the desktop directory
# desktop = os.path.join(os.path.join(os.environ['USERPROFILE']), 'OneDrive')
# os.chdir(desktop)
#
# # creating a http request handler
# Handler = http.server.SimpleHTTPRequestHandler
#
# # getting the hostname and IP address
# hostname = socket.gethostname()
# s = socket.socket(socket.AF_INET, socket.SOCK_DGRAM)
# s.connect(("8.8.8.8", 80))
# IP = "http://" + s.getsockname()[0] + ":" + str(PORT)
# link = IP
#
# # converting the IP address into a QR code
# url = pyqrcode.create(link)
# url.svg("myqr.svg", scale=8)
#
# # function to start the server and open the browser
# def start_server():
#     try:
#         with socketserver.TCPServer(("", PORT), Handler) as httpd:
#             print("Server running at port", PORT)
#             print("Type this in your browser:", IP)
#             print("or use the QR code")
#             httpd.serve_forever()
#     except Exception as e:
#         messagebox.showerror("Error", f"Failed to start server: {e}")
#
# # creating a tkinter window
# window = tk.Tk()
# window.title("QR Server")
#
# # function to open the QR code in default browser
# def open_qr():
#     webbrowser.open("myqr.svg")
#
# # function to start the server and display IP
# def start_server_and_display():
#     start_server()
#     messagebox.showinfo("Server Info", f"Server running at:\n{IP}")
#
# # adding a star button to start the server
# start_button = tk.Button(window, text="Start Server", command=start_server_and_display)
# start_button.pack(pady=10)
#
# # adding a button to open the QR code
# qr_button = tk.Button(window, text="Open QR Code", command=open_qr)
# qr_button.pack(pady=5)
#
# # adding a quit button to close the window
# quit_button = tk.Button(window, text="Quit", command=window.quit)
# quit_button.pack(pady=5)
#
# # running the tkinter event loop
# window.mainloop()


# import necessary modules
# import http.server
# import socket
# import socketserver
# import webbrowser
# import pyqrcode
# import os
#
# # for tkinter GUI
# import tkinter as tk
# from tkinter import messagebox
#
# # setting up the port
# PORT = 8010
#
# # getting the desktop directory
# desktop = os.path.join(os.path.join(os.environ['USERPROFILE']), 'OneDrive')
# os.chdir(desktop)
#
# # creating a http request handler
# Handler = http.server.SimpleHTTPRequestHandler
#
# # getting the hostname and IP address
# hostname = socket.gethostname()
# s = socket.socket(socket.AF_INET, socket.SOCK_DGRAM)
# s.connect(("8.8.8.8", 80))
# IP = "http://" + s.getsockname()[0] + ":" + str(PORT)
# link = IP
#
# # converting the IP address into a QR code
# url = pyqrcode.create(link)
# url.svg("myqr.svg", scale=8)
#
# # function to start the server and open the browser
# def start_server():
#     try:
#         with socketserver.TCPServer(("", PORT), Handler) as httpd:
#             print("Server running at port", PORT)
#             print("Type this in your browser:", IP)
#             print("or use the QR code")
#             httpd.serve_forever()
#     except Exception as e:
#         messagebox.showerror("Error", f"Failed to start server: {e}")
#
# # creating a tkinter window
# window = tk.Tk()
# window.title("QR Server")
#
# # set background color
# window.configure(bg='dark green')
#
# # function to open the QR code in default browser
# def open_qr():
#     webbrowser.open("myqr.svg")
#
# # function to start the server and display IP
# def start_server_and_display():
#     start_server()
#     messagebox.showinfo("Server Info", f"Server running at:\n{IP}")
#
# # adding a start button to start the server
# start_button = tk.Button(window, text="Start Server", command=start_server_and_display)
# start_button.pack(pady=10)
#
# # adding a button to open the QR code
# qr_button = tk.Button(window, text="Open QR Code", command=open_qr)
# qr_button.pack(pady=5)
#
# # adding a quit button to close the window
# quit_button = tk.Button(window, text="Quit", command=window.quit)
# quit_button.pack(pady=5)
#
# # running the tkinter event loop
# window.mainloop()




import http.server
import socket
import socketserver
import webbrowser
import pyqrcode
import os

# for tkinter GUI
import tkinter as tk
from tkinter import messagebox

# setting up the port
PORT = 8010

# getting the desktop directory
desktop = os.path.join(os.path.join(os.environ['USERPROFILE']), 'OneDrive')
os.chdir(desktop)

# creating a http request handler
Handler = http.server.SimpleHTTPRequestHandler

# getting the hostname and IP address
hostname = socket.gethostname()
s = socket.socket(socket.AF_INET, socket.SOCK_DGRAM)
s.connect(("8.8.8.8", 80))
IP = "http://" + s.getsockname()[0] + ":" + str(PORT)
link = IP

# converting the IP address into a QR code
url = pyqrcode.create(link)
url.svg("myqr.svg", scale=8)

# function to start the server and open the browser
def start_server():
    try:
        with socketserver.TCPServer(("", PORT), Handler) as httpd:
            print("Server running at port", PORT)
            print("Type this in your browser:", IP)
            print("or use the QR code")
            httpd.serve_forever()
    except Exception as e:
        messagebox.showerror("Error", f"Failed to start server: {e}")

# creating a tkinter window
window = tk.Tk()
window.title("QR Server")

# set background color to light blue
window.configure(bg='light blue')

# function to open the QR code in default browser
def open_qr():
    webbrowser.open("myqr.svg")

# function to start the server and display IP
def start_server_and_display():
    start_server()
    messagebox.showinfo("Server Info", f"Server running at:\n{IP}")

# adding a start button to start the server
start_button = tk.Button(window, text="Start Server", command=start_server_and_display)
start_button.pack(pady=10)

# adding a button to open the QR code
qr_button = tk.Button(window, text="Open QR Code", command=open_qr)
qr_button.pack(pady=5)

# adding a quit button to close the window
quit_button = tk.Button(window, text="Quit", command=window.quit)
quit_button.pack(pady=5)

# running the tkinter event loop
window.mainloop()





