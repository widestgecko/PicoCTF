## Descripción
This vault uses for-loops and byte arrays.The source code for this vault is here: [VaultDoor3.java](https://challenge-files.picoctf.net/c_fickle_tempest/5351a2aa13dcef1a4a661eccae345babfce30ae13eea5f3b35f4a4ae5cbb23da/VaultDoor3.java)

## Solución

Uso el siguiente codigo de python para reconstruir la password: def checkPassword(password):     if not len(password) == 32:         return False     buffer = [""] * 32

    for i in range(8):        buffer[i] = password[i]

    for i in range(8, 16):         buffer[i] = password[23 - i]

    for i in range(16, 32, 2):         buffer[i] = password[46 - i]

    for i in range(31, 16, -2):         buffer[i] = password[i]

    print(''.join(buffer))  # Combine and print the reconstructed password

checkPassword("jU5t_a_sna_3lpm18gb4c_u_4_m2r640")

picoCTF{jU5t_a_s1mpl3_an4gr4m_4_u_c2b680}