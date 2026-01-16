import React, { useState } from 'react';
import { Menu, X, ChevronDown, MapPin, Users, BookOpen, Lightbulb, Award, Calendar, ArrowRight, ExternalLink } from 'lucide-react';

export default function TechLibertyChamber() {
  const [mobileMenuOpen, setMobileMenuOpen] = useState(false);
  const [formData, setFormData] = useState({
    name: '',
    email: '',
    category: '',
    message: ''
  });

  const stats = [
    { number: '1,080+', label: 'Youth Trained' },
    { number: '9', label: 'Workshops Delivered' },
    { number: '10+', label: 'Innovation Prototypes' },
    { number: '1,500+', label: 'Platform Users' },
    { number: '50,000+', label: 'Digital Impressions' },
    { number: '77%', label: 'Skills Improvement' }
  ];

  const workshops = [
    {
      title: 'Digital Liberty & Web3 Fundamentals',
      description: 'Blockchain basics, digital liberty, online financial safety',
      locations: ['Kigali', 'Musanze', 'Rusizi']
    },
    {
      title: 'Crypto Safety & Entrepreneurship',
      description: 'Ethical crypto use, entrepreneurship, civic-tech problem solving',
      locations: ['Huye', 'Rubavu', 'Nyagatare']
    },
    {
      title: 'Innovation Challenge & Policy Dialogue',
      description: 'Youth pitch challenge, digital rights discussion, innovation mentoring',
      locations: ['Rwamagana', 'Kigali', 'Musanze']
    }
  ];

  const programs = [
    {
      icon: BookOpen,
      title: 'Learning Platform',
      description: 'Access self-paced Web3 courses, video tutorials, and interactive resources',
      link: '#platform'
    },
    {
      icon: Lightbulb,
      title: 'Innovation Challenge',
      description: 'Annual youth pitch competition with mentorship and incubation support',
      link: '#innovation'
    },
    {
      icon: Users,
      title: 'Liberty & Tech Clubs',
      description: 'Start or join a club at your university to build digital skills together',
      link: '#clubs'
    },
    {
      icon: Award,
      title: 'Policy Advocacy',
      description: 'Contribute to digital rights research and youth-led policy dialogue',
      link: '#policy'
    }
  ];

  const successStories = [
    {
      name: 'Uwase Marie',
      location: 'Kigali, Rwanda',
      achievement: 'Launched civic-tech prototype for local governance transparency',
      quote: 'TLC gave me the knowledge and confidence to build solutions for my community',
      improvement: '85% skills improvement'
    },
    {
      name: 'Mugabo Eric',
      location: 'Musanze, Rwanda',
      achievement: 'Developed blockchain-based supply chain tracker for local farmers',
      quote: 'From workshop participant to blockchain developer in 6 months',
      improvement: '92% skills improvement'
    },
    {
      name: 'Umutoni Grace',
      location: 'Rusizi, Rwanda',
      achievement: 'Created digital wallet safety education program for youth',
      quote: 'Now I help others avoid the scams I once feared myself',
      improvement: '78% skills improvement'
    }
  ];

  const handleSubmit = (e) => {
    e.preventDefault();
    alert('Thank you! We will contact you soon.');
    setFormData({ name: '', email: '', category: '', message: '' });
  };

  return (
    <div className="min-h-screen bg-white">
      {/* Header */}
      <header className="bg-gradient-to-r from-blue-900 to-purple-900 text-white sticky top-0 z-50 shadow-lg">
        <div className="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
          <div className="flex justify-between items-center py-4">
            <div className="flex items-center space-x-3">
              <div className="w-12 h-12 bg-white rounded-lg flex items-center justify-center">
                <span className="text-2xl font-bold text-blue-900">TLC</span>
              </div>
              <div>
                <h1 className="text-xl font-bold">Tech Liberty Chamber</h1>
                <p className="text-xs text-blue-200">Great Lakes Region</p>
              </div>
            </div>

            {/* Desktop Navigation */}
            <nav className="hidden md:flex space-x-8">
              <a href="#home" className="hover:text-blue-300 transition">Home</a>
              <a href="#programs" className="hover:text-blue-300 transition">Programs</a>
              <a href="#workshops" className="hover:text-blue-300 transition">Workshops</a>
              <a href="#stories" className="hover:text-blue-300 transition">Success Stories</a>
              <a href="#contact" className="hover:text-blue-300 transition">Contact</a>
            </nav>

            <div className="hidden md:flex space-x-3">
              <button className="bg-orange-500 hover:bg-orange-600 px-6 py-2 rounded-lg font-semibold transition">
                Register Now
              </button>
            </div>

            {/* Mobile menu button */}
            <button 
              className="md:hidden"
              onClick={() => setMobileMenuOpen(!mobileMenuOpen)}
            >
              {mobileMenuOpen ? <X size={24} /> : <Menu size={24} />}
            </button>
          </div>

          {/* Mobile Navigation */}
          {mobileMenuOpen && (
            <nav className="md:hidden pb-4 space-y-2">
              <a href="#home" className="block py-2 hover:text-blue-300">Home</a>
              <a href="#programs" className="block py-2 hover:text-blue-300">Programs</a>
              <a href="#workshops" className="block py-2 hover:text-blue-300">Workshops</a>
              <a href="#stories" className="block py-2 hover:text-blue-300">Success Stories</a>
              <a href="#contact" className="block py-2 hover:text-blue-300">Contact</a>
              <button className="w-full bg-orange-500 hover:bg-orange-600 px-6 py-2 rounded-lg font-semibold mt-2">
                Register Now
              </button>
            </nav>
          )}
        </div>
      </header>

      {/* Hero Section */}
      <section id="home" className="relative bg-gradient-to-br from-blue-900 via-purple-900 to-blue-800 text-white py-20">
        <div className="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
          <div className="grid md:grid-cols-2 gap-12 items-center">
            <div>
              <h2 className="text-5xl font-bold mb-6 leading-tight">
                Empowering African Youth Through Digital Liberty
              </h2>
              <p className="text-xl mb-8 text-blue-100">
                Building the future of Web3, blockchain literacy, and digital rights across Rwanda and the Great Lakes region
              </p>
              <div className="flex flex-wrap gap-4">
                <button className="bg-orange-500 hover:bg-orange-600 px-8 py-3 rounded-lg font-semibold text-lg transition flex items-center">
                  Join a Workshop <ArrowRight className="ml-2" size={20} />
                </button>
                <button className="bg-white text-blue-900 hover:bg-gray-100 px-8 py-3 rounded-lg font-semibold text-lg transition">
                  Access Platform
                </button>
              </div>
            </div>
            <div className="hidden md:block">
              <div className="bg-white/10 backdrop-blur-lg rounded-2xl p-8 border border-white/20">
                <h3 className="text-2xl font-bold mb-4">Our Impact</h3>
                <div className="space-y-4">
                  {stats.slice(0, 4).map((stat, index) => (
                    <div key={index} className="flex justify-between items-center">
                      <span className="text-blue-200">{stat.label}</span>
                      <span className="text-3xl font-bold">{stat.number}</span>
                    </div>
                  ))}
                </div>
              </div>
            </div>
          </div>
        </div>
      </section>

      {/* Mission Section */}
      <section className="py-16 bg-gray-50">
        <div className="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
          <div className="max-w-4xl mx-auto text-center">
            <h3 className="text-3xl font-bold text-gray-900 mb-6">Our Mission</h3>
            <p className="text-lg text-gray-700 leading-relaxed mb-8">
              Tech Liberty Chamber bridges the critical gap in digital financial literacy, Web3 education, and digital rights awareness among African youth. We combine grassroots education, entrepreneurial incubation, and policy advocacy to empower young people with the skills and civic awareness needed to thrive in the digital economy—safely, responsibly, and with full liberty.
            </p>
            <div className="grid md:grid-cols-3 gap-6 mt-12">
              <div className="bg-white p-6 rounded-xl shadow-md">
                <div className="text-4xl mb-4">🎓</div>
                <h4 className="font-bold text-lg mb-2">Education</h4>
                <p className="text-gray-600 text-sm">Practical blockchain & Web3 training</p>
              </div>
              <div className="bg-white p-6 rounded-xl shadow-md">
                <div className="text-4xl mb-4">🚀</div>
                <h4 className="font-bold text-lg mb-2">Innovation</h4>
                <p className="text-gray-600 text-sm">Entrepreneurial incubation support</p>
              </div>
              <div className="bg-white p-6 rounded-xl shadow-md">
                <div className="text-4xl mb-4">📢</div>
                <h4 className="font-bold text-lg mb-2">Advocacy</h4>
                <p className="text-gray-600 text-sm">Youth voice in digital policy</p>
              </div>
            </div>
          </div>
        </div>
      </section>

      {/* Stats Section */}
      <section className="py-16 bg-blue-900 text-white">
        <div className="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
          <h3 className="text-3xl font-bold text-center mb-12">Impact by the Numbers</h3>
          <div className="grid grid-cols-2 md:grid-cols-3 lg:grid-cols-6 gap-8">
            {stats.map((stat, index) => (
              <div key={index} className="text-center">
                <div className="text-4xl font-bold text-orange-400 mb-2">{stat.number}</div>
                <div className="text-sm text-blue-200">{stat.label}</div>
              </div>
            ))}
          </div>
        </div>
      </section>

      {/* Programs Section */}
      <section id="programs" className="py-16">
        <div className="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
          <h3 className="text-4xl font-bold text-center mb-4">Our Programs</h3>
          <p className="text-center text-gray-600 mb-12 max-w-2xl mx-auto">
            Comprehensive pathways to digital literacy, innovation, and civic engagement
          </p>
          <div className="grid md:grid-cols-2 lg:grid-cols-4 gap-8">
            {programs.map((program, index) => {
              const Icon = program.icon;
              return (
                <div key={index} className="bg-white rounded-xl shadow-lg p-6 hover:shadow-xl transition border-t-4 border-blue-500">
                  <Icon className="text-blue-600 mb-4" size={40} />
                  <h4 className="text-xl font-bold mb-3">{program.title}</h4>
                  <p className="text-gray-600 mb-4">{program.description}</p>
                  <a href={program.link} className="text-blue-600 font-semibold hover:text-blue-800 flex items-center">
                    Learn More <ArrowRight className="ml-2" size={16} />
                  </a>
                </div>
              );
            })}
          </div>
        </div>
      </section>

      {/* Workshops Section */}
      <section id="workshops" className="py-16 bg-gray-50">
        <div className="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
          <h3 className="text-4xl font-bold text-center mb-4">Workshop Series</h3>
          <p className="text-center text-gray-600 mb-12 max-w-2xl mx-auto">
            Hands-on training across 7 cities in Rwanda
          </p>
          <div className="grid md:grid-cols-3 gap-8">
            {workshops.map((workshop, index) => (
              <div key={index} className="bg-white rounded-xl shadow-lg p-6 hover:shadow-xl transition">
                <div className="bg-gradient-to-r from-blue-500 to-purple-500 text-white rounded-lg p-4 mb-4">
                  <Calendar className="mb-2" size={32} />
                  <h4 className="font-bold text-lg">{workshop.title}</h4>
                </div>
                <p className="text-gray-700 mb-4">{workshop.description}</p>
                <div className="border-t pt-4">
                  <p className="text-sm text-gray-500 mb-2 flex items-center">
                    <MapPin size={16} className="mr-2" /> Locations:
                  </p>
                  <div className="flex flex-wrap gap-2">
                    {workshop.locations.map((location, idx) => (
                      <span key={idx} className="bg-blue-100 text-blue-800 text-xs px-3 py-1 rounded-full">
                        {location}
                      </span>
                    ))}
                  </div>
                </div>
              </div>
            ))}
          </div>
          <div className="text-center mt-12">
            <button className="bg-orange-500 hover:bg-orange-600 text-white px-8 py-3 rounded-lg font-semibold text-lg transition">
              Register for Next Workshop
            </button>
          </div>
        </div>
      </section>

      {/* Success Stories */}
      <section id="stories" className="py-16">
        <div className="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
          <h3 className="text-4xl font-bold text-center mb-4">Success Stories</h3>
          <p className="text-center text-gray-600 mb-12 max-w-2xl mx-auto">
            From workshop participants to digital innovators
          </p>
          <div className="grid md:grid-cols-3 gap-8">
            {successStories.map((story, index) => (
              <div key={index} className="bg-gradient-to-br from-blue-50 to-purple-50 rounded-xl p-6 shadow-lg">
                <div className="w-20 h-20 bg-gradient-to-br from-blue-500 to-purple-500 rounded-full mx-auto mb-4 flex items-center justify-center text-white text-2xl font-bold">
                  {story.name.split(' ')[0][0]}{story.name.split(' ')[1][0]}
                </div>
                <h4 className="font-bold text-lg text-center mb-1">{story.name}</h4>
                <p className="text-sm text-gray-500 text-center mb-4 flex items-center justify-center">
                  <MapPin size={14} className="mr-1" /> {story.location}
                </p>
                <div className="bg-white rounded-lg p-4 mb-4">
                  <p className="text-sm text-gray-700 italic">"{story.quote}"</p>
                </div>
                <p className="text-sm font-semibold text-blue-900 mb-2">{story.achievement}</p>
                <div className="bg-green-100 text-green-800 text-xs px-3 py-1 rounded-full inline-block">
                  {story.improvement}
                </div>
              </div>
            ))}
          </div>
        </div>
      </section>

      {/* Contact Section */}
      <section id="contact" className="py-16 bg-gray-50">
        <div className="max-w-4xl mx-auto px-4 sm:px-6 lg:px-8">
          <h3 className="text-4xl font-bold text-center mb-4">Get Involved</h3>
          <p className="text-center text-gray-600 mb-12">
            Join us in empowering African youth through digital liberty
          </p>
          <div className="bg-white rounded-xl shadow-lg p-8">
            <div className="space-y-6">
              <div>
                <label className="block text-sm font-semibold mb-2">Name</label>
                <input
                  type="text"
                  value={formData.name}
                  onChange={(e) => setFormData({...formData, name: e.target.value})}
                  className="w-full px-4 py-2 border border-gray-300 rounded-lg focus:ring-2 focus:ring-blue-500 focus:border-transparent"
                />
              </div>
              <div>
                <label className="block text-sm font-semibold mb-2">Email</label>
                <input
                  type="email"
                  value={formData.email}
                  onChange={(e) => setFormData({...formData, email: e.target.value})}
                  className="w-full px-4 py-2 border border-gray-300 rounded-lg focus:ring-2 focus:ring-blue-500 focus:border-transparent"
                />
              </div>
              <div>
                <label className="block text-sm font-semibold mb-2">I am a:</label>
                <select
                  value={formData.category}
                  onChange={(e) => setFormData({...formData, category: e.target.value})}
                  className="w-full px-4 py-2 border border-gray-300 rounded-lg focus:ring-2 focus:ring-blue-500 focus:border-transparent"
                >
                  <option value="">Select...</option>
                  <option value="student">Student</option>
                  <option value="entrepreneur">Entrepreneur</option>
                  <option value="mentor">Mentor</option>
                  <option value="partner">Partner</option>
                  <option value="media">Media</option>
                </select>
              </div>
              <div>
                <label className="block text-sm font-semibold mb-2">Message</label>
                <textarea
                  value={formData.message}
                  onChange={(e) => setFormData({...formData, message: e.target.value})}
                  rows={4}
                  className="w-full px-4 py-2 border border-gray-300 rounded-lg focus:ring-2 focus:ring-blue-500 focus:border-transparent"
                ></textarea>
              </div>
              <button
                onClick={handleSubmit}
                className="w-full bg-gradient-to-r from-blue-600 to-purple-600 hover:from-blue-700 hover:to-purple-700 text-white px-8 py-3 rounded-lg font-semibold text-lg transition"
              >
                Send Message
              </button>
            </div>
          </div>
        </div>
      </section>

      {/* Footer */}
      <footer className="bg-gray-900 text-white py-12">
        <div className="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
          <div className="grid md:grid-cols-4 gap-8">
            <div>
              <h4 className="font-bold text-lg mb-4">Tech Liberty Chamber</h4>
              <p className="text-gray-400 text-sm">
                Empowering youth across Rwanda and the Great Lakes region through digital literacy and innovation
              </p>
            </div>
            <div>
              <h4 className="font-bold mb-4">Programs</h4>
              <ul className="space-y-2 text-sm">
                <li><a href="#" className="text-gray-400 hover:text-white">Workshops</a></li>
                <li><a href="#" className="text-gray-400 hover:text-white">Learning Platform</a></li>
                <li><a href="#" className="text-gray-400 hover:text-white">Innovation Challenge</a></li>
                <li><a href="#" className="text-gray-400 hover:text-white">Liberty & Tech Clubs</a></li>
              </ul>
            </div>
            <div>
              <h4 className="font-bold mb-4">Resources</h4>
              <ul className="space-y-2 text-sm">
                <li><a href="#" className="text-gray-400 hover:text-white">Policy Briefs</a></li>
                <li><a href="#" className="text-gray-400 hover:text-white">Blog</a></li>
                <li><a href="#" className="text-gray-400 hover:text-white">FAQ</a></li>
                <li><a href="#" className="text-gray-400 hover:text-white">Success Stories</a></li>
              </ul>
            </div>
            <div>
              <h4 className="font-bold mb-4">Contact</h4>
              <ul className="space-y-2 text-sm text-gray-400">
                <li>hirwatresor@studentsforliberty.org</li>
                <li>+250 787 717 843</li>
                <li>Kigali, Rwanda</li>
              </ul>
            </div>
          </div>
          <div className="border-t border-gray-800 mt-8 pt-8 text-center text-sm text-gray-400">
            <p>© 2026 Tech Liberty Chamber. Supported by Students For Liberty - Great Lakes Region</p>
          </div>
        </div>
      </footer>
    </div>
  );
}
