# 1. Update sistem dan instal dependencies
sudo apt-get update
sudo apt-get install build-essential cmake libssl-dev libboost-all-dev git -y

# 2. Clone TON miner repository
git clone https://github.com/ton-blockchain/ton-miner.git
cd ton-miner

# 3. Build TON miner
cmake .
make

# 4. Jalankan miner dengan memasukkan alamat wallet dan pool mining dari pool yang dipilih
# Contoh pool: tonwhales.com dengan port: 4000
./tonminer --wallet UQAzkgj6wE5qTH0_IECzPrOGaAaLMgOL07ivbJcu-OjXODTy --pool tonwhales.com --port 4000

# 5. Monitoring mining (opsional)
tail -f miner.log
