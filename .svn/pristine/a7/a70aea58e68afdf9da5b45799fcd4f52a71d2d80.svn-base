#include <iostream>
#include <vector>
#include <string>
#include <fstream>


std::vector<std::string> ReadFile( std::string inFileName, int lineCount );


int main()
{
	std::cout << "ReadFile test:\n";
	std::vector<std::string> inFileVector = ReadFile( "test.txt", 20 );

	// Print each line to verify we got the data.
	for( size_t i = 0; i < inFileVector.size(); i++ )
	{
		std::cout << "\t" << inFileVector.at( i ) << std::endl;
	}
}


std::vector<std::string> ReadFile( std::string fileName, int lineCount )
{
	std::string line;
	std::vector<std::string> inVector;
	std::ifstream myfile( fileName );
	if( myfile.is_open() )
	{
		while( getline( myfile, line ) )
		{
			inVector.push_back( line );
		}
		myfile.close();
	}
	else
	{
		std::cout << "Unable to open \"" << fileName << "\"" << std::endl;
	}
	return inVector;
}
