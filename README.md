import React from 'react';

const App = () => {
  return (
    <div className="font-sans">
      <Navbar />
      <Hero />
      <About />
      <Education />
      <Skills />
      <Contact />
    </div>
  );
};

const Navbar = () => (
  <nav className="bg-gray-900 text-white p-4 flex justify-between">
    <h1 className="text-xl font-bold">Aditya's Portfolio</h1>
    <div className="space-x-4">
      <a href="#about">About</a>
      <a href="#education">Education</a>
      <a href="#skills">Skills</a>
      <a href="#contact">Contact</a>
    </div>
  </nav>
);

const Hero = () => (
  <section className="h-screen flex flex-col justify-center items-center text-center bg-blue-600 text-white">
    <h1 className="text-5xl font-bold">Aditya Kumar Singh</h1>
    <p className="text-lg mt-4">Aspiring Software Developer | B.Tech IT Student at Sharda University</p>
    <a href="#contact" className="mt-6 px-4 py-2 bg-white text-blue-600 font-semibold rounded hover:scale-105 transition">
      Contact Me
    </a>
  </section>
);

const About = () => (
  <section id="about" className="p-8 max-w-3xl mx-auto">
    <h2 className="text-3xl font-semibold mb-4">About Me</h2>
    <p>
      I am a Software Engineering student at Sharda University with a focus on Software Development. Passionate about crafting innovative solutions and aspiring to excel in technology.
    </p>
  </section>
);

const Education = () => (
  <section id="education" className="p-8 max-w-3xl mx-auto">
    <h2 className="text-3xl font-semibold mb-4">Education</h2>
    <ul className="space-y-4">
      <li>
        <strong>Sharda University</strong><br />
        B.Tech in Information Technology<br />
        Score: 7.3 CGPA
      </li>
      <li>
        <strong>Class XII – CBSE</strong><br />
        65.8% (2023)
      </li>
      <li>
        <strong>Class X – CBSE</strong><br />
        61.2% (2021)
      </li>
    </ul>
  </section>
);

const Skills = () => {
  const skills = ['Software Development', 'Software Engineering', 'Node.js', 'Full Stack Web Development'];

  return (
    <section id="skills" className="bg-gray-100 p-8">
      <h2 className="text-3xl font-semibold mb-4 text-center">Skills</h2>
      <div className="flex flex-wrap justify-center gap-4">
        {skills.map((skill, idx) => (
          <span key={idx} className="px-4 py-2 bg-blue-200 text-blue-800 rounded-full">
            {skill}
          </span>
        ))}
      </div>
    </section>
  );
};

const Contact = () => (
  <section id="contact" className="p-8 max-w-xl mx-auto">
    <h2 className="text-3xl font-semibold mb-4">Get In Touch</h2>
    <p className="mb-4">📧 <a href="mailto:adityakmr0304@gmail.com" className="text-blue-600">adityakmr0304@gmail.com</a></p>
    <p>📞 +91-9097777237</p>
  </section>
);

export default App;
