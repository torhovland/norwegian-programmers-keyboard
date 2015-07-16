Add the following to the end of the following file:
/usr/share/X11/xkb/symbols/no

partial alphanumeric_keys
xkb_symbols "norprog" {

    include "no(basic)"

    name[Group1]="Norwegian programmer's keyboard";

    key <TLDE> { [ semicolon,	      bar,      section	] };
    key <AE01>	{ [         1,     exclam ]	};
    key <AE02>	{ [         2,   quotedbl,           at ]	};
    key <AE03>	{ [         3, numbersign,     sterling ]	};
    key <AE04>	{ [         4,     dollar ]	};
    key <AE05>	{ [         5,    percent ]	};
    key <AE06>	{ [         6,  ampersand ]	};
    key <AE07>	{ [         7,   asterisk,    braceleft, slash ]	};
    key <AE08>	{ [         8,       less,  bracketleft, parenleft ]	};
    key <AE09>	{ [         9,    greater, bracketright, parenright ]	};
    key <AE10>	{ [         0,      equal,   braceright ]	};
    key <AE11>	{ [ bracketleft, bracketright, plus, question ]	};
    key <AE12>	{ [        ae,         AE,    backslash, dead_grave ]	};

    key <AD03>	{ [         d,          D, EuroSign ]	};
    key <AD04>	{ [         u,          U, asciicircum ]	};
    key <AD05>	{ [         f,          F ]	};
    key <AD07>	{ [         j,          J ]	};
    key <AD08>	{ [         k,          K ]	};
    key <AD09>	{ [         l,          L ]	};
    key <AD10>	{ [     colon,       plus ]	};
    key <AD11>	{ [     aring,      Aring ]	};
    key <AD12>	{ [    oslash,     Oslash,     diaeresis,  asciicircum ]	};

    key <AC01>	{ [         a,          A,       dead_grave ]	};
    key <AC02>	{ [         s,          S,       dead_acute ]	};
    key <AC03>	{ [         e,          E,      diaeresis ]	};
    key <AC04>	{ [         t,          T,  asciitilde ]	};
    key <AC07>	{ [         r,          R ]	};
    key <AC08>	{ [         i,          I ]	};
    key <AC09>	{ [         o,          O ]	};
    key <AC10>	{ [         p,          P ]	};
    key <AC11>	{ [ parenleft, parenright ]	};
    key <BKSL>	{ [     slash,  backslash,    apostrophe,    asterisk ]	};

    key <LSGT>	{ [ braceleft, braceright,   less,     greater ]	};
    key <AB07>	{ [         m,          M, mu ] };
    key <AB08>	{ [     comma, apostrophe, semicolon ] };
    key <AB09>	{ [    period,   question, colon ] };
    key <AB10>	{ [     minus, underscore ]	};

    key <CAPS> { [ BackSpace ] };
    key <BKSP>  { [ Caps_Lock ] };
};

Put the following variant into:
/usr/share/X11/xkb/rules/evdev.xml

        <variant>
          <configItem>
            <name>norprog</name>
            <description>Norwegian (Programmer's Keyboard)</description>
          </configItem>
        </variant>

Then run:

cd /var/lib/xkb/
sudo rm *.xkm

Go to Keyboard settings and find the layout there.
