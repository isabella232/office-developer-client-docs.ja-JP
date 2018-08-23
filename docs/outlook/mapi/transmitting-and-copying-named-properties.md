---
title: 名前付きプロパティの送信とコピー
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 37075cfc-461d-4983-9045-d9f1da6739be
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: a5d2244270463fcc2fe0a9786112590e741a8a66
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804125"
---
# <a name="transmitting-and-copying-named-properties"></a>名前付きプロパティの送信とコピー

  
  
**適用対象**: Outlook 
  
名前付きプロパティが送信されるたびに移動すると、コピー、または、名前は変わりませんが目的のオブジェクトへのマッピングに準拠する識別子を変更する必要があります。 この規則の唯一の例外は、ソースとターゲットのシグネチャを持つ、同じマッピング、ときに再マッピングを不要にすることです。
  
ターゲットで動作する適切な識別子を転送の名前付きプロパティの名前を再マップするトランスポート プロバイダーの役割です。 適切なマッピングとは、宛先に送信側のトランスポート プロバイダーを知ることはできません。名前を送信し、動作する識別子にマップするのには受信側のトランスポート プロバイダーに依存して、必要があります。 TNEF の MAPI 実装では、トランスポート プロバイダーの名前付きプロパティの再割り当てを処理します。 トランスポート プロバイダー再マッピングを手動で処理か、TNEF の実装を使用します。 
  
これらのプロパティがメッセージ ストア間でコピーされると、名前付きプロパティの再マッピングのような必要があります。 ただし、メッセージ ストア プロバイダーは、識別子のマッピング先の名前を取得できる、ため、プロパティをすぐに再マップし、メッセージの保存先のストアに依存していませんが。 
  
## <a name="see-also"></a>関連項目



[MAPI ���O�t���v���p�e�B](mapi-named-properties.md)

