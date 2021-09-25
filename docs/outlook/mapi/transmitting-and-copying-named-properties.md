---
title: 名前付きプロパティの送信とコピー
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 37075cfc-461d-4983-9045-d9f1da6739be
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 9e040277b82c0a946fbb55907ce823301351c44f
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59578460"
---
# <a name="transmitting-and-copying-named-properties"></a>名前付きプロパティの送信とコピー

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
名前付きプロパティが送信、移動、またはコピーされるたびに、名前は定数のままですが、識別子は変更して移動先オブジェクトのマッピングに従う必要があります。 このルールの唯一の例外は、コピー元と宛先が同じマッピング署名を持ち、再マップを不要にしている場合です。
  
転送先で動作する適切な識別子に、送信された名前付きプロパティの名前を再マップする必要があります。 送信トランスポート プロバイダーは、宛先に正しいマッピングが何を示すのかわかりません。名前を送信し、受信トランスポート プロバイダーに依存して、動作する識別子にマップする必要があります。 TNEF の MAPI 実装は、トランスポート プロバイダーの名前付きプロパティの再マップを処理します。 トランスポート プロバイダーは、手動で再マップを処理するか、TNEF 実装を使用できます。 
  
名前付きプロパティの同様の再マップは、これらのプロパティがメッセージ ストア間でコピーされる場合に発生する必要があります。 ただし、メッセージ ストア プロバイダーは、名前を取得して宛先の識別子マッピングを取得できるので、プロパティをすぐ再マップし、宛先メッセージ ストアに依存する必要が生じない場合があります。 
  
## <a name="see-also"></a>関連項目



[MAPI ���O�t���v���p�e�B](mapi-named-properties.md)

