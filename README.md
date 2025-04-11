import React, { useEffect } from 'react';

const UPIPaymentGateway = () => {
  useEffect(() => {
    // Add interactive elements
    const components = document.querySelectorAll('.component');
    
    components.forEach(component => {
      component.addEventListener('click', function() {
        // Create pulse effect
        const pulse = document.createElement('div');
        pulse.classList.add('pulse');
        this.appendChild(pulse);
        
        // Remove pulse after animation completes
        setTimeout(() => {
          pulse.remove();
        }, 2000);
      });
    });
  }, []);

  return (
    <div className="container p-4 mx-auto" style={{
      backgroundColor: '#0a0e17',
      color: '#e6f1ff',
      backgroundImage: `
        radial-gradient(circle at 10% 10%, rgba(0, 168, 255, 0.1) 0%, transparent 30%),
        radial-gradient(circle at 90% 20%, rgba(174, 0, 255, 0.1) 0%, transparent 30%),
        radial-gradient(circle at 50% 50%, rgba(0, 255, 157, 0.05) 0%, transparent 60%),
        linear-gradient(to bottom, #0a0e17, #080812)
      `,
      backgroundAttachment: 'fixed',
      minHeight: '100vh'
    }}>
      <header className="text-center mb-12 p-4 relative">
        <h1 className="text-4xl mb-2" style={{
          background: 'linear-gradient(90deg, #00a8ff, #ae00ff)',
          WebkitBackgroundClip: 'text',
          WebkitTextFillColor: 'transparent',
          textShadow: '0 0 10px rgba(174, 0, 255, 0.2)'
        }}>Centralized UPI Payment Gateway System</h1>
        <p className="text-lg mx-auto max-w-2xl text-opacity-80">
          A comprehensive simulation of India's Unified Payments Interface (UPI) ecosystem with advanced security features
        </p>
        <div className="mt-4">
          <span className="inline-block bg-opacity-70 text-xs px-3 py-1 m-1 rounded-full border border-opacity-20" style={{ borderColor: '#ff004c', color: '#ff004c' }}>
            Blockchain Ledger
          </span>
          <span className="inline-block bg-opacity-70 text-xs px-3 py-1 m-1 rounded-full border border-opacity-20" style={{ borderColor: '#00ff9d', color: '#00ff9d' }}>
            SHA-256 Hashing
          </span>
          <span className="inline-block bg-opacity-70 text-xs px-3 py-1 m-1 rounded-full border border-opacity-20" style={{ borderColor: '#ae00ff', color: '#ae00ff' }}>
            SPECK Encryption
          </span>
          <span className="inline-block bg-opacity-70 text-xs px-3 py-1 m-1 rounded-full border border-opacity-20" style={{ borderColor: '#ffae00', color: '#ffae00' }}>
            Quantum Attack Simulation
          </span>
        </div>
        <div className="absolute bottom-0 left-1/4 w-1/2 h-0.5" style={{ background: 'linear-gradient(90deg, transparent, #00a8ff, #ae00ff, transparent)' }}></div>
      </header>
      
      <div className="flex flex-col items-center my-12">
        <h2 className="text-2xl mb-4" style={{ color: '#00ff9d', textShadow: '0 0 5px rgba(0, 255, 157, 0.3)' }}>
          System Architecture
        </h2>
        
        <div className="relative w-full h-96 rounded-xl overflow-hidden bg-opacity-70 shadow-xl border border-opacity-10" style={{ 
          backgroundColor: 'rgba(10, 14, 23, 0.7)',
          borderColor: 'rgba(230, 241, 255, 0.1)'
        }}>
          {/* Grid Background */}
          <div className="absolute inset-0" style={{ 
            backgroundImage: `
              linear-gradient(rgba(230, 241, 255, 0.05) 1px, transparent 1px),
              linear-gradient(90deg, rgba(230, 241, 255, 0.05) 1px, transparent 1px)
            `,
            backgroundSize: '40px 40px'
          }}></div>
          
          {/* Components */}
          <div className="component absolute flex items-center justify-center w-32 h-16 rounded-lg border transition-all cursor-pointer text-center font-bold z-10"
            style={{ 
              top: '250px', 
              left: '80px',
              backgroundColor: 'rgba(10, 14, 23, 0.85)',
              borderColor: '#00a8ff',
              boxShadow: '0 0 10px #00a8ff, 0 0 20px rgba(0, 168, 255, 0.5)'
            }}>
            User Client
          </div>
          
          <div className="component absolute flex items-center justify-center w-32 h-16 rounded-lg border transition-all cursor-pointer text-center font-bold z-10"
            style={{ 
              top: '250px', 
              left: '50%',
              transform: 'translateX(-50%)',
              backgroundColor: 'rgba(10, 14, 23, 0.85)',
              borderColor: '#ae00ff',
              boxShadow: '0 0 10px #ae00ff, 0 0 20px rgba(174, 0, 255, 0.5)'
            }}>
            UPI Machine
          </div>
          
          <div className="component absolute flex items-center justify-center w-32 h-16 rounded-lg border transition-all cursor-pointer text-center font-bold z-10"
            style={{ 
              top: '120px', 
              left: '50%',
              transform: 'translateX(-50%)',
              backgroundColor: 'rgba(10, 14, 23, 0.85)',
              borderColor: '#00ff9d',
              boxShadow: '0 0 10px #00ff9d, 0 0 20px rgba(0, 255, 157, 0.5)'
            }}>
            Bank Server
          </div>
          
          <div className="component absolute flex items-center justify-center w-32 h-16 rounded-lg border transition-all cursor-pointer text-center font-bold z-10"
            style={{ 
              top: '120px', 
              right: '80px',
              backgroundColor: 'rgba(10, 14, 23, 0.85)',
              borderColor: '#ff004c',
              boxShadow: '0 0 10px #ff004c, 0 0 20px rgba(255, 0, 76, 0.5)'
            }}>
            Blockchain Ledger
          </div>
          
          <div className="component absolute flex items-center justify-center w-32 h-16 rounded-lg border transition-all cursor-pointer text-center font-bold z-10"
            style={{ 
              top: '250px', 
              right: '80px',
              backgroundColor: 'rgba(10, 14, 23, 0.85)',
              borderColor: '#ffae00',
              boxShadow: '0 0 10px #ffae00, 0 0 20px rgba(255, 174, 0, 0.5)'
            }}>
            Merchant
          </div>
          
          {/* SVG Connections */}
          <svg className="absolute inset-0 w-full h-full z-10 pointer-events-none">
            {/* User to UPI */}
            <path d="M 150,250 C 200,250 200,250 300,250" stroke="#00a8ff" strokeWidth="2" fill="none" 
              style={{ strokeDasharray: 10, animation: 'flow 1s linear infinite' }} />
            
            {/* UPI to Bank */}
            <path d="M 400,250 C 400,200 400,200 400,155" stroke="#ae00ff" strokeWidth="2" fill="none" 
              style={{ strokeDasharray: 10, animation: 'flow 1s linear infinite' }} />
            
            {/* Bank to Blockchain */}
            <path d="M 470,120 C 520,120 520,120 570,120" stroke="#00ff9d" strokeWidth="2" fill="none" 
              style={{ strokeDasharray: 10, animation: 'flow 1s linear infinite' }} />
            
            {/* Bank to UPI (response) */}
            <path d="M 400,155 C 400,200 400,200 400,245" stroke="#00ff9d" strokeWidth="2" fill="none" 
              style={{ strokeDasharray: 10, animation: 'flow 1s linear infinite' }} />
            
            {/* UPI to User (response) */}
            <path d="M 330,250 C 250,250 250,250 150,250" stroke="#ae00ff" strokeWidth="2" fill="none" 
              style={{ strokeDasharray: 10, animation: 'flow 1s linear infinite' }} />
            
            {/* UPI to Merchant */}
            <path d="M 470,250 C 520,250 520,250 570,250" stroke="#ae00ff" strokeWidth="2" fill="none" 
              style={{ strokeDasharray: 10, animation: 'flow 1s linear infinite' }} />
          </svg>
          
          {/* Data Flow Animations */}
          <style dangerouslySetInnerHTML={{ __html: `
            @keyframes transaction-flow {
              0% { left: 150px; top: 250px; opacity: 0; }
              10% { opacity: 1; }
              45% { left: 50%; top: 250px; transform: translateX(-50%); }
              90% { opacity: 1; }
              100% { left: 50%; top: 120px; transform: translateX(-50%); opacity: 0; }
            }
            
            @keyframes verification-flow {
              0% { left: 50%; top: 120px; transform: translateX(-50%); opacity: 0; }
              10% { opacity: 1; }
              90% { opacity: 1; }
              100% { left: calc(100% - 150px); top: 120px; opacity: 0; }
            }
            
            @keyframes confirmation-flow {
              0% { left: 50%; top: 120px; transform: translateX(-50%); opacity: 0; }
              10% { opacity: 1; }
              45% { left: 50%; top: 250px; transform: translateX(-50%); }
              90% { opacity: 1; }
              100% { left: calc(100% - 150px); top: 250px; opacity: 0; }
            }
            
            @keyframes blockchain-flow {
              0% { left: 50%; top: 120px; transform: translateX(-50%); opacity: 0; }
              20% { opacity: 1; }
              80% { opacity: 1; }
              100% { left: calc(100% - 150px); top: 120px; opacity: 0; }
            }
            
            @keyframes flow {
              from { stroke-dashoffset: 20; }
              to { stroke-dashoffset: 0; }
            }
            
            @keyframes alert-blink {
              0%, 100% { opacity: 0.7; }
              50% { opacity: 1; }
            }
            
            @keyframes pulse {
              0% {
                transform: scale(0);
                opacity: 0.8;
              }
              100% {
                transform: scale(2);
                opacity: 0;
              }
            }
            
            .pulse {
              position: absolute;
              top: 0;
              left: 0;
              width: 100%;
              height: 100%;
              border-radius: 50%;
              background-color: rgba(255, 255, 255, 0.3);
              animation: pulse 2s infinite;
              pointer-events: none;
            }
          `}} />
          
          <div className="absolute z-20 pointer-events-none">
            <div className="absolute w-3 h-3 rounded-full" style={{ 
              backgroundColor: '#00a8ff',
              boxShadow: '0 0 8px #00a8ff',
              animation: 'transaction-flow 8s linear infinite'
            }}></div>
            
            <div className="absolute w-3 h-3 rounded-full" style={{ 
              backgroundColor: '#00ff9d',
              boxShadow: '0 0 8px #00ff9d',
              animation: 'verification-flow 6s linear infinite'
            }}></div>
            
            <div className="absolute w-3 h-3 rounded-full" style={{ 
              backgroundColor: '#ae00ff',
              boxShadow: '0 0 8px #ae00ff',
              animation: 'confirmation-flow 7s linear infinite'
            }}></div>
            
            <div className="absolute w-3 h-3 rounded-full" style={{ 
              backgroundColor: '#ff004c',
              boxShadow: '0 0 8px #ff004c',
              animation: 'blockchain-flow 5s linear infinite'
            }}></div>
          </div>
          
          <div className="absolute bottom-12 left-1/2 transform -translate-x-1/2 px-6 py-3 rounded flex items-center text-sm"
            style={{ 
              backgroundColor: 'rgba(255, 0, 76, 0.15)',
              borderColor: '#ff004c',
              border: '1px solid #ff004c',
              boxShadow: '0 0 10px #ff004c, 0 0 20px rgba(255, 0, 76, 0.5)',
              animation: 'alert-blink 3s infinite'
            }}>
            <span className="mr-2" style={{ color: '#ff004c' }}>⚠</span>
            Quantum Attack Simulation Available
          </div>
        </div>
      </div>
      
      <div className="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8 mt-12">
        <div className="bg-opacity-80 rounded-xl p-6 relative border border-opacity-10" 
          style={{ 
            backgroundColor: 'rgba(10, 14, 23, 0.8)',
            borderColor: 'rgba(230, 241, 255, 0.1)'
          }}>
          <div className="absolute top-0 left-0 w-1 h-full" style={{ 
            backgroundColor: '#00a8ff',
            boxShadow: '0 0 10px #00a8ff, 0 0 20px rgba(0, 168, 255, 0.5)'
          }}></div>
          <div className="absolute top-4 right-4 text-4xl font-bold opacity-20">01</div>
          <div className="text-lg font-bold mb-4 pr-8" style={{ color: '#00a8ff' }}>QR Code Scanning</div>
          <div className="text-sm leading-relaxed text-opacity-80">
            User scans the QR code from the merchant terminal to initiate a payment. The QR code contains the encrypted Virtual Merchant ID (VMID).
          </div>
        </div>
        
        <div className="bg-opacity-80 rounded-xl p-6 relative border border-opacity-10" 
          style={{ 
            backgroundColor: 'rgba(10, 14, 23, 0.8)',
            borderColor: 'rgba(230, 241, 255, 0.1)'
          }}>
          <div className="absolute top-0 left-0 w-1 h-full" style={{ 
            backgroundColor: '#ae00ff',
            boxShadow: '0 0 10px #ae00ff, 0 0 20px rgba(174, 0, 255, 0.5)'
          }}></div>
          <div className="absolute top-4 right-4 text-4xl font-bold opacity-20">02</div>
          <div className="text-lg font-bold mb-4 pr-8" style={{ color: '#ae00ff' }}>Payment Initiation</div>
          <div className="text-sm leading-relaxed text-opacity-80">
            User enters their MMID, PIN, and transaction amount. The UPI machine processes this information and decrypts the VMID using SPECK algorithm.
          </div>
        </div>
        
        <div className="bg-opacity-80 rounded-xl p-6 relative border border-opacity-10" 
          style={{ 
            backgroundColor: 'rgba(10, 14, 23, 0.8)',
            borderColor: 'rgba(230, 241, 255, 0.1)'
          }}>
          <div className="absolute top-0 left-0 w-1 h-full" style={{ 
            backgroundColor: '#00ff9d',
            boxShadow: '0 0 10px #00ff9d, 0 0 20px rgba(0, 255, 157, 0.5)'
          }}></div>
          <div className="absolute top-4 right-4 text-4xl font-bold opacity-20">03</div>
          <div className="text-lg font-bold mb-4 pr-8" style={{ color: '#00ff9d' }}>Transaction Verification</div>
          <div className="text-sm leading-relaxed text-opacity-80">
            Bank server verifies user credentials, checks account balance, and validates the merchant ID to ensure secure transaction processing.
          </div>
        </div>
        
        <div className="bg-opacity-80 rounded-xl p-6 relative border border-opacity-10" 
          style={{ 
            backgroundColor: 'rgba(10, 14, 23, 0.8)',
            borderColor: 'rgba(230, 241, 255, 0.1)'
          }}>
          <div className="absolute top-0 left-0 w-1 h-full" style={{ 
            backgroundColor: '#ff004c',
            boxShadow: '0 0 10px #ff004c, 0 0 20px rgba(255, 0, 76, 0.5)'
          }}></div>
          <div className="absolute top-4 right-4 text-4xl font-bold opacity-20">04</div>
          <div className="text-lg font-bold mb-4 pr-8" style={{ color: '#ff004c' }}>Blockchain Recording</div>
          <div className="text-sm leading-relaxed text-opacity-80">
            All transaction details are recorded in an immutable blockchain ledger, ensuring transparency and preventing tampering with transaction history.
          </div>
        </div>
        
        <div className="bg-opacity-80 rounded-xl p-6 relative border border-opacity-10" 
          style={{ 
            backgroundColor: 'rgba(10, 14, 23, 0.8)',
            borderColor: 'rgba(230, 241, 255, 0.1)'
          }}>
          <div className="absolute top-0 left-0 w-1 h-full" style={{ 
            backgroundColor: '#00a8ff',
            boxShadow: '0 0 10px #00a8ff, 0 0 20px rgba(0, 168, 255, 0.5)'
          }}></div>
          <div className="absolute top-4 right-4 text-4xl font-bold opacity-20">05</div>
          <div className="text-lg font-bold mb-4 pr-8" style={{ color: '#00a8ff' }}>Confirmation</div>
          <div className="text-sm leading-relaxed text-opacity-80">
            User receives confirmation of successful payment, along with updated account balance and transaction details for record-keeping.
          </div>
        </div>
        
        <div className="bg-opacity-80 rounded-xl p-6 relative border border-opacity-10" 
          style={{ 
            backgroundColor: 'rgba(10, 14, 23, 0.8)',
            borderColor: 'rgba(230, 241, 255, 0.1)'
          }}>
          <div className="absolute top-0 left-0 w-1 h-full" style={{ 
            backgroundColor: '#00ff9d',
            boxShadow: '0 0 10px #00ff9d, 0 0 20px rgba(0, 255, 157, 0.5)'
          }}></div>
          <div className="absolute top-4 right-4 text-4xl font-bold opacity-20">06</div>
          <div className="text-lg font-bold mb-4 pr-8" style={{ color: '#00ff9d' }}>Quantum Security</div>
          <div className="text-sm leading-relaxed text-opacity-80">
            The system includes optional quantum attack simulation to demonstrate potential vulnerabilities in traditional PIN-based security systems.
          </div>
        </div>
      </div>
      
      <div className="text-center mt-12 pt-8 text-sm text-opacity-60 relative">
        <div className="absolute top-0 left-1/4 w-1/2 h-px" style={{ 
          background: 'linear-gradient(90deg, transparent, rgba(230, 241, 255, 0.1), transparent)'
        }}></div>
        © 2025 Centralized UPI Payment Gateway System | BITS F463 Cryptography Term Project
      </div>
    </div>
  );
};

export default UPIPaymentGateway;
