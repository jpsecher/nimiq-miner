# Docker container for stand-alone Nimiq miner

## Plan

- [x] Get a Nimiq miner up and running locally.
- [ ] Make the Nimiq account configurable.
- [ ] Get the miner to connect to a mining pool.
- [ ] Make a HTTP endpoint that reports the status of the miner.

## Notes

    $ cd src/miner
    $ docker build -t jpsecher/nimiq-miner .

It seem the blockchain is located under `/main-full-consensus/`, and the wallet is under `/wallet/`. And `/peer-key/`.  So the miner should be started in dedicated, mounted directory.

[I 19:41:52] Node: Nimiq NodeJS Client starting (network=main, dumb, miner=true, rpc=false, metrics=false)
[I 19:41:52] Node: Peer address: dumb:///0e71698d356d8bd4e411786dc25d2cf9 - public key: 2a385d1a672423086a3e9f32dc5173aa23f099ffb678f04102eb7adcc5400965
[I 19:41:52] Node: Managing wallets []
[I 19:41:52] Node: Wallet initialized for address NQ46 UGCV 26ET 160E E9VU 5XHG QSXH YSUY 2RVQ. Balance: 0 NIM
[I 19:41:52] Node: Blockchain state: height=1, headHash=Jkqvik+YKKdsVQY12geOtGYwahifzANxC+6fZJyGnRI=
[I 19:41:53] Node: Connected to wss://seed-4.nimiq-network.com:8443/2e3dab4410d597b7da762a36aef42a4d
[I 19:41:54] Node: Connected to wss://edaxmfbpwglpshrw.ga:8443/4e21d7490f53867f3b11d85191374225
[I 19:41:55] Node: Connected to wss://us2.nimiq.skypool.org:8080/c88ea9b7008a0f15d933b105ffdf5550
[I 19:41:56] Node: Now at block: 100
[I 19:41:56] Node: Connected to wss://seed-3.nimiq.com:8443/0a1988babbcc8544c593e0d3002db1f3
[I 19:41:57] Node: Connected to wss://yarrig.nimiq.by:8080/32276f5897a29447d40a90445873a915
[I 19:41:57] Node: Connected to wss://nimiq.mopsus.com:5653/1a69fc0f077f23e9ae4da0f7cb9a3a74
[I 19:41:57] Node: Now at block: 200
[I 19:41:58] Node: Connected to wss://tqbwwzdirkodwync.gq:8443/b130f2b114ddc10af8f7e9823e40eac0
[I 19:41:59] Node: Connected to wss://battery.deathbypptx.com:8080/c0bd832dd083824fc8b90ebd76d82856
[I 19:41:59] Node: Now at block: 300
[I 19:42:00] Node: Now at block: 400
[I 19:42:00] Node: Connected to wss://seed-1.nimiq.com:8443/dfd55fe967d6c0ca707d3a73ec31e4ac
[I 19:42:00] Node: Connected to wss://nimiq.scottynordstrom.com:18443/bd96a15593fb8354397ee14d5fc24794
[I 19:42:01] Node: Now at block: 500
[I 19:42:02] Node: Connected to wss://gileowcbrcrbjdyv.cf:8443/11395e6076d71b1c7eb8a3daf7493121
[I 19:42:02] Node: Now at block: 600
[I 19:42:03] Node: Connected to wss://nim1.lightbulblist.com:8443/245208cf3464c808af820ff6d646b267
[I 19:42:03] Node: Now at block: 700
[I 19:42:04] Node: Now at block: 800
[I 19:42:05] Node: Now at block: 900
[I 19:42:06] Node: Now at block: 1000
[I 19:42:07] Node: Now at block: 1100
[I 19:42:08] Node: Now at block: 1200
[I 19:42:09] Node: Now at block: 1300
[I 19:42:10] Node: Now at block: 1400
[I 19:42:11] Node: Now at block: 1500
[I 19:42:12] Node: Now at block: 1600
[I 19:42:13] Node: Now at block: 1700
[I 19:42:14] Node: Now at block: 1800
[I 19:42:15] Node: Now at block: 1900
[I 19:42:16] Node: Now at block: 2000
[I 19:42:18] Node: Now at block: 2100
[I 19:42:19] Node: Now at block: 2200
[I 19:42:20] Node: Now at block: 2300
[I 19:42:21] Node: Now at block: 2400
[I 19:42:23] Node: Disconnected from wss://seed-4.nimiq-network.com:8443/2e3dab4410d597b7da762a36aef42a4d
[I 19:42:23] Node: Now at block: 2500
[I 19:42:24] Node: Connected to wss://seed-5.nimiq-network.com:8443/56d39daf18c010acf56d4f5ff24819c3
[I 19:42:24] Node: Now at block: 2600
[I 19:42:25] Node: Now at block: 2700
[I 19:42:26] Node: Now at block: 2800
[I 19:42:27] Node: Now at block: 2900
[I 19:42:28] Node: Now at block: 3000
[I 19:42:29] Node: Now at block: 3100
[I 19:42:30] Node: Now at block: 3200
[I 19:42:31] Node: Now at block: 3300
[I 19:42:32] Node: Now at block: 3400
[I 19:42:35] Node: Now at block: 3500
[I 19:42:36] Node: Now at block: 3600
[I 19:42:37] Node: Now at block: 3700
[I 19:42:38] Node: Now at block: 3800
[I 19:42:39] Node: Now at block: 3900
[I 19:42:41] Node: Now at block: 4000
[I 19:42:42] Node: Now at block: 4100
[I 19:42:43] Node: Now at block: 4200
[I 19:42:44] Node: Now at block: 4300
[I 19:42:44] Node: Now at block: 4400
[I 19:42:46] Node: Now at block: 4500
[I 19:42:47] Node: Now at block: 4600
[I 19:42:49] Node: Now at block: 4700
[I 19:42:50] Node: Now at block: 4800
[I 19:42:53] Node: Now at block: 4900
[I 19:42:54] Node: Now at block: 5000
[I 19:42:55] Node: Now at block: 5100
[I 19:42:56] Node: Now at block: 5200
[I 19:42:57] Node: Now at block: 5300
[I 19:42:58] Node: Now at block: 5400
[I 19:43:00] Node: Now at block: 5500
[I 19:43:01] Node: Now at block: 5600
[I 19:43:02] Node: Now at block: 5700
[I 19:43:03] Node: Now at block: 5800
[I 19:43:04] Node: Now at block: 5900
[I 19:43:05] Node: Now at block: 6000
[I 19:43:06] Node: Now at block: 6100
[I 19:43:08] Node: Now at block: 6200
[I 19:43:10] Node: Now at block: 6300
[I 19:43:11] Node: Now at block: 6400
[I 19:43:13] Node: Now at block: 6500
[I 19:43:14] Node: Now at block: 6600
[I 19:43:15] Node: Now at block: 6700
[I 19:43:16] Node: Now at block: 6800
[I 19:43:17] Node: Now at block: 6900
[I 19:43:18] Node: Now at block: 7000
[I 19:43:20] Node: Now at block: 7100
[I 19:43:21] Node: Now at block: 7200
[I 19:43:22] Node: Now at block: 7300
[I 19:43:23] Node: Now at block: 7400
[I 19:43:25] Node: Now at block: 7500
[I 19:43:26] Node: Now at block: 7600
[I 19:43:28] Node: Now at block: 7700
[I 19:43:30] Node: Now at block: 7800
[I 19:43:32] Node: Now at block: 7900
[I 19:43:33] Node: Now at block: 8000
[I 19:43:34] Node: Now at block: 8100
[I 19:43:35] Node: Now at block: 8200
[I 19:43:37] Node: Now at block: 8300
[I 19:43:38] Node: Now at block: 8400
[I 19:43:39] Node: Now at block: 8500
[I 19:43:40] Node: Now at block: 8600
[I 19:43:41] Node: Now at block: 8700
[I 19:43:42] Node: Now at block: 8800
[I 19:43:44] Node: Now at block: 8900
[I 19:43:45] Node: Now at block: 9000
[I 19:43:46] Node: Now at block: 9100
[I 19:43:49] Node: Now at block: 9200
[I 19:43:50] Node: Now at block: 9300
[I 19:43:51] Node: Now at block: 9400
[I 19:43:52] Node: Now at block: 9500
[I 19:43:53] Node: Now at block: 9600
[I 19:43:54] Node: Now at block: 9700
[I 19:43:55] Node: Disconnected from wss://nimiq.scottynordstrom.com:18443/bd96a15593fb8354397ee14d5fc24794
[I 19:43:55] Node: Now at block: 9800
[I 19:43:57] Node: Now at block: 9900
[I 19:43:58] Node: Now at block: 10000
[I 19:43:59] Node: Now at block: 10100
[I 19:44:00] Node: Now at block: 10200
[I 19:44:01] Node: Now at block: 10300
[I 19:44:02] Node: Now at block: 10400
[I 19:44:04] Node: Now at block: 10500
[I 19:44:06] Node: Now at block: 10600
[I 19:44:07] Node: Now at block: 10700
[I 19:44:09] Node: Now at block: 10800
[I 19:44:10] Node: Now at block: 10900
[I 19:44:11] Node: Connected to wss://nimiq.phbase.de:8443/a1f2d54fbc23bec2d0826efca824ffbf
[I 19:44:11] Node: Now at block: 11000
[I 19:44:12] Node: Now at block: 11100
[I 19:44:13] Node: Now at block: 11200
[I 19:44:14] Node: Now at block: 11300
[I 19:44:15] Node: Now at block: 11400
[I 19:44:17] Node: Now at block: 11500
[I 19:44:18] Node: Now at block: 11600
[I 19:44:19] Node: Now at block: 11700
[I 19:44:20] Node: Now at block: 11800
[I 19:44:22] Node: Now at block: 11900
[I 19:44:23] Node: Now at block: 12000
[I 19:44:25] Node: Now at block: 12100
[I 19:44:26] Node: Now at block: 12200
[I 19:44:27] Node: Now at block: 12300
[I 19:44:28] Node: Now at block: 12400
[I 19:44:30] Node: Now at block: 12500
[I 19:44:31] Node: Now at block: 12600
[I 19:44:32] Node: Now at block: 12700
[I 19:44:33] Node: Now at block: 12800
[I 19:44:34] Node: Now at block: 12900
[I 19:44:36] Node: Now at block: 13000
[I 19:44:37] Node: Now at block: 13100
[I 19:44:38] Node: Now at block: 13200
[I 19:44:39] Node: Now at block: 13300
[I 19:44:40] Node: Now at block: 13400
[I 19:44:43] Node: Now at block: 13500
[I 19:44:44] Node: Now at block: 13600
[I 19:44:46] Node: Now at block: 13700
[I 19:44:47] Node: Now at block: 13800
[I 19:44:48] Node: Now at block: 13900
[I 19:44:49] Node: Now at block: 14000
[I 19:44:50] Node: Now at block: 14100
[I 19:44:51] Node: Now at block: 14200
[I 19:44:53] Node: Now at block: 14300
[I 19:44:54] Node: Now at block: 14400
[I 19:44:55] Node: Disconnected from wss://gileowcbrcrbjdyv.cf:8443/11395e6076d71b1c7eb8a3daf7493121
[I 19:44:55] Node: Now at block: 14500
[I 19:44:56] Node: Connected to wss://gileowcbrcrbjdyv.tk:8443/5af764e8eb26a14d777694c853491239
[I 19:44:57] Node: Now at block: 14600
[I 19:44:58] Node: Now at block: 14700
[I 19:44:59] Node: Now at block: 14800
[I 19:45:01] Node: Now at block: 14900
[I 19:45:03] Node: Now at block: 15000
[I 19:45:04] Node: Now at block: 15100
[I 19:45:05] Node: Now at block: 15200
[I 19:45:06] Node: Now at block: 15300
[I 19:45:07] Node: Now at block: 15400
[I 19:45:09] Node: Now at block: 15500
[I 19:45:10] Node: Now at block: 15600
[I 19:45:11] Node: Now at block: 15700
[I 19:45:12] Node: Now at block: 15800
[I 19:45:13] Node: Now at block: 15900
[I 19:45:14] Node: Now at block: 16000
[I 19:45:16] Node: Now at block: 16100
[I 19:45:17] Node: Now at block: 16200
[I 19:45:18] Node: Now at block: 16300
[I 19:45:20] Node: Now at block: 16400
[I 19:45:22] Node: Now at block: 16500
[I 19:45:23] Node: Now at block: 16600
[I 19:45:24] Node: Now at block: 16700
[I 19:45:25] Node: Now at block: 16800
[I 19:45:27] Node: Now at block: 16900
[I 19:45:28] Node: Now at block: 17000
[I 19:45:29] Node: Now at block: 17100
[I 19:45:30] Node: Now at block: 17200
[I 19:45:31] Node: Now at block: 17300
[I 19:45:32] Node: Now at block: 17400
[I 19:45:34] Node: Now at block: 17500
[I 19:45:35] Node: Now at block: 17600
[I 19:45:36] Node: Now at block: 17700
[I 19:45:38] Node: Now at block: 17800
[I 19:45:39] Node: Now at block: 17900
[I 19:45:41] Node: Now at block: 18000
[I 19:45:42] Node: Now at block: 18100
[I 19:45:43] Node: Now at block: 18200
[I 19:45:44] Node: Now at block: 18300
[I 19:45:45] Node: Now at block: 18400
[I 19:45:47] Node: Now at block: 18500
[I 19:45:48] Node: Now at block: 18600
[I 19:45:49] Node: Now at block: 18700
[I 19:45:50] Node: Now at block: 18800
[I 19:45:51] Node: Now at block: 18900
[I 19:45:53] Node: Now at block: 19000
[I 19:45:54] Node: Now at block: 19100
[I 19:45:57] Node: Now at block: 19200
[I 19:45:58] Node: Now at block: 19300
[I 19:45:59] Node: Now at block: 19400
[I 19:46:00] Node: Now at block: 19500
[I 19:46:01] Node: Now at block: 19600
[I 19:46:03] Node: Now at block: 19700
[I 19:46:04] Node: Now at block: 19800
[I 19:46:05] Node: Now at block: 19900
[I 19:46:06] Node: Now at block: 20000
[I 19:46:07] Node: Now at block: 20100
[I 19:46:09] Node: Now at block: 20200
[I 19:46:10] Node: Now at block: 20300
[I 19:46:11] Node: Now at block: 20400
[I 19:46:12] Node: Now at block: 20500
[I 19:46:14] Node: Now at block: 20600
[I 19:46:16] Node: Now at block: 20700
[I 19:46:17] Node: Now at block: 20800
[I 19:46:18] Node: Now at block: 20900
[I 19:46:19] Node: Now at block: 21000
[I 19:46:21] Node: Now at block: 21100
[I 19:46:22] Node: Now at block: 21200
[I 19:46:23] Node: Now at block: 21300
[I 19:46:24] Node: Now at block: 21400
[I 19:46:25] Node: Now at block: 21500
[I 19:46:26] Node: Now at block: 21600
[I 19:46:27] Node: Now at block: 21700
[I 19:46:29] Node: Now at block: 21800
[I 19:46:30] Node: Now at block: 21900
[I 19:46:31] Node: Now at block: 22000
[I 19:46:34] Node: Now at block: 22100
[I 19:46:35] Node: Now at block: 22200
[I 19:46:36] Node: Now at block: 22300
[I 19:46:37] Node: Now at block: 22400
[I 19:46:39] Node: Now at block: 22500
[I 19:46:40] Node: Now at block: 22600
[I 19:46:41] Node: Now at block: 22700
[I 19:46:42] Node: Now at block: 22800
[I 19:46:43] Node: Now at block: 22900
[I 19:46:45] Node: Now at block: 23000
[I 19:46:46] Node: Now at block: 23100
[I 19:46:47] Node: Now at block: 23200
[I 19:46:48] Node: Now at block: 23300
[I 19:46:49] Node: Now at block: 23400
[I 19:46:52] Node: Now at block: 23500
[I 19:46:53] Node: Now at block: 23600
[I 19:46:54] Node: Now at block: 23700
[I 19:46:55] Node: Now at block: 23800
[I 19:46:56] Node: Now at block: 23900
[I 19:46:58] Node: Now at block: 24000
[I 19:46:59] Node: Now at block: 24100
[I 19:47:00] Node: Now at block: 24200
[I 19:47:01] Node: Now at block: 24300
[I 19:47:02] Node: Now at block: 24400
[I 19:47:04] Node: Now at block: 24500
[I 19:47:05] Node: Now at block: 24600
[I 19:47:06] Node: Now at block: 24700
[I 19:47:07] Node: Now at block: 24800
[I 19:47:09] Node: Now at block: 24900
[I 19:47:10] Node: Now at block: 25000
[I 19:47:11] Node: Now at block: 25100
[I 19:47:12] Node: Now at block: 25200
[I 19:47:13] Node: Now at block: 25300
[I 19:47:15] Node: Now at block: 25400
[I 19:47:16] Node: Now at block: 25500
[I 19:47:18] Node: Now at block: 25600
[I 19:47:19] Node: Now at block: 25700
[I 19:47:20] Node: Now at block: 25800
[I 19:47:21] Node: Now at block: 25900
[I 19:47:23] Node: Now at block: 26000
[I 19:47:24] Node: Now at block: 26100
[I 19:47:25] Node: Now at block: 26200
[I 19:47:26] Node: Now at block: 26300
[I 19:47:28] Node: Now at block: 26400
[I 19:47:29] Node: Now at block: 26500
[I 19:47:30] Node: Now at block: 26600
[I 19:47:32] Node: Now at block: 26700
[I 19:47:33] Node: Now at block: 26800
[I 19:47:34] Node: Now at block: 26900
[I 19:47:35] Node: Now at block: 27000
[I 19:47:37] Node: Now at block: 27100
[I 19:47:38] Node: Now at block: 27200
[I 19:47:39] Node: Now at block: 27300
[I 19:47:40] Node: Now at block: 27400
[I 19:47:42] Node: Now at block: 27500
[I 19:47:43] Node: Now at block: 27600
[I 19:47:44] Node: Now at block: 27700
[I 19:47:46] Node: Now at block: 27800
[I 19:47:48] Node: Now at block: 27900
[I 19:47:49] Node: Now at block: 28000
[I 19:47:50] Node: Now at block: 28100
[I 19:47:52] Node: Now at block: 28200
[I 19:47:53] Node: Now at block: 28300
[I 19:47:54] Node: Now at block: 28400
[I 19:47:56] Node: Now at block: 28500
[I 19:47:57] Node: Now at block: 28600
[I 19:47:58] Node: Now at block: 28700
[I 19:48:00] Node: Now at block: 28800
[I 19:48:01] Node: Now at block: 28900
[I 19:48:02] Node: Now at block: 29000
[I 19:48:04] Node: Now at block: 29100
[I 19:48:06] Node: Now at block: 29200
[I 19:48:07] Node: Now at block: 29300
[I 19:48:09] Node: Now at block: 29400
[I 19:48:10] Node: Now at block: 29500
[I 19:48:11] Node: Now at block: 29600
[I 19:48:13] Node: Now at block: 29700
[I 19:48:14] Node: Now at block: 29800
[I 19:48:15] Node: Now at block: 29900
[I 19:48:16] Node: Now at block: 30000
[I 19:48:18] Node: Now at block: 30100
[I 19:48:19] Node: Now at block: 30200
[I 19:48:20] Node: Now at block: 30300
[I 19:48:21] Node: Now at block: 30400
[I 19:48:23] Node: Now at block: 30500
[I 19:48:24] Node: Now at block: 30600
[I 19:48:26] Node: Now at block: 30700
[I 19:48:28] Node: Now at block: 30800
[I 19:48:29] Node: Now at block: 30900
[I 19:48:31] Node: Now at block: 31000
[I 19:48:32] Node: Now at block: 31100
[I 19:48:33] Node: Now at block: 31200
[I 19:48:34] Node: Now at block: 31300
[I 19:48:35] Node: Now at block: 31400
[I 19:48:37] Node: Now at block: 31500
[I 19:48:38] Node: Now at block: 31600
[I 19:48:39] Node: Now at block: 31700
[I 19:48:40] Node: Now at block: 31800
[I 19:48:42] Node: Now at block: 31900
[I 19:48:44] Node: Now at block: 32000
[I 19:48:46] Node: Now at block: 32100
[I 19:48:47] Node: Now at block: 32200
[I 19:48:49] Node: Now at block: 32300
[I 19:48:50] Node: Now at block: 32400
[I 19:48:51] Node: Now at block: 32500
[I 19:48:53] Node: Now at block: 32600
[I 19:48:54] Node: Now at block: 32700
[I 19:48:55] Node: Now at block: 32800
[I 19:48:57] Node: Now at block: 32900
[I 19:48:58] Node: Now at block: 33000
[I 19:49:00] Node: Now at block: 33100
[I 19:49:01] Node: Now at block: 33200
[I 19:49:02] Node: Now at block: 33300
[I 19:49:04] Node: Now at block: 33400
[I 19:49:05] Node: Now at block: 33500
[I 19:49:08] Node: Now at block: 33600
[I 19:49:09] Node: Now at block: 33700
[I 19:49:10] Node: Now at block: 33800
[I 19:49:12] Node: Now at block: 33900
[I 19:49:13] Node: Now at block: 34000
[I 19:49:15] Node: Now at block: 34100
[I 19:49:16] Node: Now at block: 34200
[I 19:49:17] Node: Now at block: 34300
[I 19:49:19] Node: Now at block: 34400
[I 19:49:20] Node: Now at block: 34500
[I 19:49:22] Node: Now at block: 34600
[I 19:49:23] Node: Now at block: 34700
[I 19:49:24] Node: Now at block: 34800
[I 19:49:25] Node: Now at block: 34900
[I 19:49:28] Node: Now at block: 35000
[I 19:49:30] Node: Now at block: 35100
[I 19:49:31] BaseConsensus: Synced with all connected peers (12), consensus established.
[I 19:49:31] Node: Blockchain full-consensus established in 458.916s.
[I 19:49:31] Node: Current state: height=35169, totalWork=184911126055.306021662, headHash=LGgGfTcBhm8NhTFid0NHGwRkiB8h22pnhzkgap65G2Q=
[I 19:49:31] Node: Now at block: 35170
[I 19:50:19] Node: Now at block: 35171
[I 19:50:39] Node: Now at block: 35172
[I 19:50:47] Node: Now at block: 35173
[I 19:50:52] Node: Now at block: 35174
[I 19:51:34] Node: Now at block: 35175
[I 19:52:02] Node: Now at block: 35176
[I 19:53:03] Node: Now at block: 35177
[I 19:54:12] Node: Now at block: 35178
[I 19:55:40] Node: Now at block: 35179
[I 19:55:53] Node: Now at block: 35180
[I 19:57:04] Node: Now at block: 35181
[I 19:58:04] Node: Now at block: 35182
[I 19:59:02] Node: Now at block: 35183
[I 19:59:49] Node: Disconnected from wss://nimiq.phbase.de:8443/a1f2d54fbc23bec2d0826efca824ffbf
[I 20:00:05] Node: Connected to wss://hk1.nimiq.skypool.org:8080/a245ebf6b7532ec484b7fa18485a14f2
[I 20:00:32] Node: Now at block: 35184
[I 20:00:56] Node: Now at block: 35185
[I 20:01:20] Node: Now at block: 35186
[I 20:01:35] Node: Now at block: 35187
[I 20:05:55] Node: Now at block: 35188
[I 20:06:25] Node: Now at block: 35189
[I 20:06:50] Node: Now at block: 35190
[I 20:07:50] Node: Disconnected from wss://yarrig.nimiq.by:8080/32276f5897a29447d40a90445873a915
[I 20:07:51] Node: Connected to wss://seed-8.nimiq.network:8443/1bcbf3534a5706129cf9cccf313b9efc
[I 20:08:56] Node: Now at block: 35191
[I 20:09:03] Node: Now at block: 35192
[I 20:09:26] Node: Now at block: 35193
[I 20:09:52] Node: Now at block: 35193
[I 20:09:52] Node: Now at block: 35194
[I 20:11:13] Node: Now at block: 35195
[I 20:12:01] Node: Now at block: 35196
[I 20:12:39] Node: Now at block: 35197
[I 20:15:00] Node: Now at block: 35198
[I 20:16:07] Node: Now at block: 35199
[I 20:17:05] Node: Now at block: 35200
[I 20:17:39] Node: Now at block: 35201
[I 20:18:48] Node: Now at block: 35202
[I 20:19:02] Node: Now at block: 35203
[I 20:19:26] Node: Now at block: 35204
[I 20:19:39] Node: Now at block: 35205
[I 20:20:42] Node: Now at block: 35206
[I 20:20:53] Node: Now at block: 35207
[I 20:21:28] Node: Now at block: 35208
[I 20:21:53] Node: Now at block: 35209
[I 20:22:07] Node: Now at block: 35210
[I 20:22:29] Node: Now at block: 35211

