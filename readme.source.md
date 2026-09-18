```aura width=800 height=250 inline align=center

<div style={{
  position: 'relative',
  display: 'flex',
  flexDirection: 'column',
  alignItems: 'center',
  justifyContent: 'center',
  width: '100%',
  height: '100%',
  background: '#201f1f',
  borderRadius: 20,
  overflow: 'hidden',
  fontFamily: 'Inter, sans-serif'
}}>

  <style>{`
    @keyframes stack-orb {
      0%, 100% {
        transform: translate(0,0);
        opacity: 0.45;
      }
      50% {
        transform: translate(18px,-14px);
        opacity: 0.7;
      }
    }

    @keyframes stack-orb-b {
      0%, 100% {
        transform: translate(0,0);
        opacity: 0.4;
      }
      50% {
        transform: translate(-14px,10px);
        opacity: 0.65;
      }
    }

    #st-o1 {
      animation: stack-orb 3s ease-in-out infinite;
    }

    #st-o2 {
      animation: stack-orb-b 3.5s ease-in-out infinite 1s;
    }

    #st-o3 {
      animation: stack-orb 2.8s ease-in-out infinite 2.5s;
    }

    #st-o4 {
      animation: stack-orb-b 3.2s ease-in-out infinite 0.5s;
    }
  `}</style>

  <svg
    width="800"
    height="250"
    style={{
      position: 'absolute',
      top: 0,
      left: 0
    }}
  >
    <defs>

      <radialGradient id="sg1" cx="50%" cy="50%" r="50%">
        <stop offset="0%" stopColor="rgba(180,100,20,0.4)" />
        <stop offset="100%" stopColor="rgba(180,100,20,0)" />
      </radialGradient>

      <radialGradient id="sg2" cx="50%" cy="50%" r="50%">
        <stop offset="0%" stopColor="rgba(160,80,10,0.35)" />
        <stop offset="100%" stopColor="rgba(160,80,10,0)" />
      </radialGradient>

      <radialGradient id="sg3" cx="50%" cy="50%" r="50%">
        <stop offset="0%" stopColor="rgba(200,130,40,0.3)" />
        <stop offset="100%" stopColor="rgba(200,130,40,0)" />
      </radialGradient>

      <radialGradient id="sg4" cx="50%" cy="50%" r="50%">
        <stop offset="0%" stopColor="rgba(150,90,20,0.3)" />
        <stop offset="100%" stopColor="rgba(150,90,20,0)" />
      </radialGradient>

    </defs>

    <ellipse
      id="st-o1"
      cx="80"
      cy="160"
      rx="160"
      ry="120"
      fill="url(#sg1)"
    />

    <ellipse
      id="st-o2"
      cx="730"
      cy="50"
      rx="150"
      ry="120"
      fill="url(#sg2)"
    />

    <ellipse
      id="st-o3"
      cx="640"
      cy="170"
      rx="140"
      ry="110"
      fill="url(#sg3)"
    />

    <ellipse
      id="st-o4"
      cx="180"
      cy="40"
      rx="130"
      ry="100"
      fill="url(#sg4)"
    />

  </svg>

  <div style={{
    display: 'flex',
    flexDirection: 'column',
    alignItems: 'center',
    gap: 12,
    zIndex: 10,
  }}>

    <div style={{
      display: 'flex',
      width: '96px',
      height: '96px',
      borderRadius: '50%',
      overflow: 'hidden',
      border: '4px solid rgba(255,120,40,0.5)',
      flexShrink: '0'
    }}>

      <img
        src="avatar.jpeg"
        style={{
          width: '96px',
          height: '96px',
          objectFit: 'cover',
          transform: 'translate(-3px, 0px)'
        }}
      />

    </div>

    <span style={{
      fontSize: '34px',
      fontWeight: '700',
      color: '#ffffff',
      letterSpacing: '-0.5px',
      textShadow: `
        0 0 10px rgba(255,255,255,0.25),
        0 0 25px rgba(255,100,30,0.2)
      `
    }}>
      Hcivekhsim
    </span>
    <div style={{
      display: 'flex',
      flexWrap: 'wrap',
      gap: 10,
      justifyContent: 'center'
    }}>

      {['Go', 'PostgreSQL', 'Docker'].map((tech, i) => (
        <span
          key={i}
          style={{
            padding: '7px 18px',
            background: 'rgba(255,255,255,0.05)',
            color: 'rgba(255,255,255,1)',
            borderRadius: 100,
            fontSize: 12,
            fontWeight: '600', 
            border: '1px solid rgba(255,120,40,0.2)',
            letterSpacing: 0.5,
            textShadow: '0 0 8px rgba(255,255,255,0.2)'
          }}
        >
          {tech}
        </span>
      ))}

    </div>

  </div>

</div>