Reason Remote Maps & Templates Archive
======================================

An open community collection of Reason Remote control surface mapping templates (`.remotemap`) covering **225+ devices**: 99 native Reason Studios stock instruments, synthesizers, samplers, drum machines, creative effects, mixer channel strips, and first-party Rack Extensions, alongside 130+ third-party Rack Extensions.

History & Provenance
-------------------
- **Original Compilation**: Generously compiled and organized by **Koshdukai** for the Reason community.
- **Repository Inception**: Published to GitHub on June 25th, 2013 by **Peter Nyboer** ([Livid Instruments](https://github.com/LividInstruments/Reason_RE_Remote_Templates)).
- **Modern Maintenance & Curation**: Forked and curated by **Edward Boraas** ([Boraas Digital](https://github.com/BoraasDigital/reason-remotemaps)) to provide a centralized, modernized archive for Reason 10, 11, 12, 13+ and modern Rack Extensions.

How to Use
----------
Each `.txt` file represents a Remotemap `Scope` definition for a specific instrument, effect, or utility:

1. **Copy the Scope snippet**: Open the text file corresponding to the device you wish to map.
2. **Add to your Controller Map**: Paste the snippet into your controller's `.remotemap` file (located in `Reason/Remote/Maps/<Manufacturer>/<Model>.remotemap`).
3. **Map your controls**:
   - Replace `_control_` with the valid control item identifier declared in your controller's `.luacodec` file (e.g., `Knob 1`, `Fader 1`, `Button 1`).
   - Remove the leading comment marks `//` to activate each mapping line:
     ```
     // Before:
     //Map	_control_	Output Level

     // After:
     Map	Knob 1	Output Level
     ```

Combining All Templates
-----------------------
If you want to concatenate all template files into a single reference document (`all.txt`):

- **macOS / Linux**:
  ```bash
  cat *.txt > all.txt
  ```

- **Windows (PowerShell)**:
  ```powershell
  Get-Content *.txt | Set-Content all.txt
  ```

- **Windows (Command Prompt)**:
  ```cmd
  copy *.txt all.txt
  ```

Contributing
------------
Contributions and updates for new Rack Extensions and Reason Studios devices are welcome! Please open a Pull Request following the established format:
```
Scope	<Manufacturer Name>	<Product ID>
//Map	_control_	<Parameter Name>
```

License
-------
This project is licensed under the [MIT License](LICENSE).