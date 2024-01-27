# pdf-merger
from PyPDF2 import PdfWriter #pip install PyPDF2
import os #built in
merger=PdfWriter()
files=os.listdir()
pdf_files=[file for file in files if file.endswith(".pdf")] #to clear clutters
for pdf in pdf_files:
  print(pdf)
  merger.append(pdf)
merger.write("merged-pdf.pdf") #new name of merged document
merger.close()
