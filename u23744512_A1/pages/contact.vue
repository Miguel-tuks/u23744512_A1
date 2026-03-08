<!--Miguel De Freitas u23744512 -->
<template>
    <div>
     <h1>Contact Me</h1>
      <form name ="contact" methd = "POST" data-netlify = "true">
       <input type = "hidden" name = "form-name" value = "contact"/>
       <label>Name</label>
       <input type = "text" name = "name" required/>
       <label>Email</label>
       <input type = "email" name = "email" required/>
       <label>Message</label>
       <textarea name="message" rows = "4" required></textarea>
       <button type ="submit">Send</button>
      </form>
    </div>
</template>