<template>
    <v-btn color="green" @click="downloadPDF">Download PDF</v-btn>
  </template>
  
  <script setup>
  const downloadPDF = () => {
    const pdfUrl = '/assets/pdf/Mostafa-Zayed-Cv.pdf'; // Replace with the URL of your PDF file
  
    fetch(pdfUrl)
      .then(response => response.blob())
      .then(blob => {
        const url = window.URL.createObjectURL(new Blob([blob]));
        const link = document.createElement('a');
        link.href = url;
        link.setAttribute('download', 'Mostafa-Zayed-Cv.pdf'); // Set the name of the downloaded file
        document.body.appendChild(link);
        link.click();
        link.parentNode.removeChild(link);
      })
      .catch(error => console.error('Error downloading PDF:', error));
  };
  </script>
  