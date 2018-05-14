# address.cpp
///Implementación de la clase address 
#include "address.h"

///Constructor base
Address::Address() {
    mainStreet = "NON";
    numExt = "NON";
    numInt = "NON";
    suburb = "NON";
    country = "NON";
}

///Constructor copia
Address::Address(const Address& a) : mainStreet(a.mainStreet), numExt(a.numExt), numInt(a.numInt), suburb(a.suburb), country(a.country) {}

///Constructor Parametrizado
Address::Address(const std::string& st, std::string&e, std::string&i, std::string& s, std::string& c) : mainStreet(st), numExt(e), numInt(i), suburb(s), country(c) { }

std::string Address::getMainStreet() {
    return mainStreet;
    }

std::string Address::getNumExt() {
    return numExt;
    }

std::string Address::getNumInt() {
    return numInt;
    }

std::string Address::getSuburb() {
    return suburb;
    }

std::string Address::getCountry() {
    return country;
    }

void Address::setMainStreet(const std::string& s) {
    mainStreet = s;
    }

void Address::setNumExt(const std::string& e) {
    numExt = e;
    }

void Address::setNumInt(const std::string& i) {
    numInt = i;
    }

void Address::setSuburb(const std::string& s) {
    suburb = s;
    }

void Address::setCountry(const std::string& c) {
    country = c;
    }

std::string Address::toString() {
    std::string result;

    result = "Calle: ";
    result += mainStreet;
    result += " NumExterior: #";
    result += numExt;
    result += " NumInterior: #";
    result += numInt;
    result += " Colonia: ";
    result += suburb;
    result += " Ciudad: ";
    result += country;

    return result;
    }
