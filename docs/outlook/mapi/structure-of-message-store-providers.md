---
title: メッセージ ストア プロバイダーの構造
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 064b2fc1-e690-43e6-95d3-a61438115de5
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: d2b6c11453ccbb127c684ccde7773bc09c1f7a49
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59578558"
---
# <a name="structure-of-message-store-providers"></a>メッセージ ストア プロバイダーの構造
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
メッセージ ストア プロバイダーは、メモリ内で実行されている場合は [、IMSProvider : IUnknown インターフェイス](imsprovideriunknown.md) です。 **IMSProvider インターフェイスを使用** すると、クライアント アプリケーションと MAPI スプーラーは、メッセージ ストアへのログオンとオフを行えます。 クライアント アプリケーションと MAPI スプーラーがメッセージ ストア内のフォルダーとメッセージにアクセスするために使用するインターフェイスは [、IMSLogon](imslogoniunknown.md) インターフェイスと [IMsgStore](imsgstoreimapiprop.md) インターフェイスです。 これらのインターフェイスは、通常、メッセージ ストアが最初にログオンするときに作成されます。ただし、メッセージ ストア DLL の [MSProviderInit](msproviderinit.md) エントリ ポイントも作成できます。 
  
**IMSLogon** インターフェイスと **IMsgStore** インターフェイスは一部のメソッドを共有しますので、これらの両方のインターフェイスから継承するクラス オブジェクトを 1 つ作成する方が簡単な場合があります。 これらのインターフェイスを個別のオブジェクトに実装し **、IMSLogon** インターフェイスと **IMsgStore** インターフェイスのメソッドから呼び出す共有メソッドを実装するヘルパー関数を DLL に記述することもできます。 
  
次の図は、実行中のメッセージ ストア内のオブジェクト階層の概要を示しています。
  
**メッセージ ストアのオブジェクト階層**
  
![メッセージ ストアのオブジェクト階層](media/storeobj.gif "メッセージ ストアのオブジェクト階層")
  
## <a name="see-also"></a>関連項目

- [MAPI メッセージ ストア プロバイダーの開発](developing-a-mapi-message-store-provider.md)

