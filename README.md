# Celestia Node

[![Go Reference](https://pkg.go.dev/badge/github.com/celestiaorg/celestia-node.svg)](https://pkg.go.dev/github.com/celestiaorg/celestia-node)
[![GitHub release (latest by date including pre-releases)](https://img.shields.io/github/v/release/celestiaorg/celestia-node)](https://github.com/celestiaorg/celestia-node/releases/latest)
[![test](https://github.com/celestiaorg/celestia-node/actions/workflows/test.yml/badge.svg)](https://github.com/celestiaorg/celestia-node/actions/workflows/test.yml)
[![lint](https://github.com/celestiaorg/celestia-node/actions/workflows/lint.yml/badge.svg)](https://github.com/celestiaorg/celestia-node/actions/workflows/lint.yml)
[![Go Report Card](https://goreportcard.com/badge/github.com/celestiaorg/celestia-node)](https://goreportcard.com/report/github.com/celestiaorg/celestia-node)
[![codecov](https://codecov.io/gh/celestiaorg/celestia-node/branch/main/graph/badge.svg?token=CWGA4RLDS9)](https://codecov.io/gh/celestiaorg/celestia-node)

Celestia'nın veri kullanılabilirliği düğüm türlerinin (`hafif` |` tam` | `köprü`) Golang uygulaması.

Yukarıda açıklanan celestia düğümü türleri, celestia veri kullanılabilirliği (DA) ağını içerir.

DA ağı, konsensüs ağından gelen blokları dinleyerek ve onları veri kullanılabilirliği örneklemesi (DAS) için sindirilebilir hale getirerek celestia çekirdekli konsensüs ağını sarar.

Continue reading [here](https://blog.celestia.org/celestia-mvp-release-data-availability-sampling-light-clients)DAS ve Celestia zincir verilerine nasıl güvenli ve ölçeklenebilir erişim sağladığı hakkında daha fazla bilgi edinmek istiyorsanız.

## Minimum requirements

| Requirement | Notes          |
|-------------|----------------|
| Go version  | 1.17 or higher |

## Sistem gereksinimleri
 

Düğüm türü başına sistem gereksinimleri için resmi belgeler sayfasına bakın: 
* [Bridge](https://docs.celestia.org/nodes/bridge-validator-node#hardware-requirements)
* [Light](https://docs.celestia.org/nodes/light-node#hardware-requirements)
* [Full](https://docs.celestia.org/nodes/full-node#hardware-requirements)

## Kurulum

```sh
git clone https://github.com/celestiaorg/celestia-node.git 
cd celestia-node
make install
```

Düğüm kurma ve gereken donanım gereksinimleri hakkında daha fazla bilgi için şu adresteki belgelerimizi ziyaret edin: <https://docs.celestia.org>.

## API docs

Celestia düğümü genel API'si belgelenmiştir [here](https://docs.celestia.org/developers/node-api/).

## Node types

- **Bridge** nodes - celestia konsensüs ağından celestia veri kullanılabilirliği (DA) ağına röle blokları
- **Full** nodes - paylaşımlar için DA ağını örnekleyerek blokları tamamen yeniden yapılandırın ve saklayın
- **Light** nodes - paylaşımlar için DA ağını örnekleyerek blok verilerinin kullanılabilirliğini doğrulayın

Daha fazla bilgi bulunabilir [here](https://github.com/celestiaorg/celestia-node/blob/main/docs/adr/adr-003-march2022-testnet.md#legend).

## Bir düğümü çalıştırın

`<node_type>` can be `bridge`, `full` or `light`.

```sh
celestia <node_type> init 
```

```sh
celestia <node_type> start
```

## Pakete özel belgeler

- [Header](./service/header/doc.go)
- [Share](./service/share/doc.go)
- [DAS](./das/doc.go)

## Davranış kodu

Davranış Kurallarımıza bakın [here](https://docs.celestia.org/community/coc).
