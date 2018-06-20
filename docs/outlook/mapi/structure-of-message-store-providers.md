---
title: メッセージ ストア プロバイダーの構造
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 064b2fc1-e690-43e6-95d3-a61438115de5
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 2f78428b8067b7937e9bd2ee36934cc29a16bfb7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804047"
---
# <a name="structure-of-message-store-providers"></a>メッセージ ストア プロバイダーの構造
  
**適用されます**: Outlook 
  
メモリで実行されているとき、メッセージのストア プロバイダーは、 [IMSProvider: IUnknown](imsprovideriunknown.md)インタ フェースです。 **IMSProvider**インタ フェースにより、クライアント アプリケーションと MAPI スプーラーを無効にして、メッセージ ・ ストアからログオンします。 フォルダーとメッセージ ・ ストア内のメッセージにアクセスするクライアント アプリケーションと MAPI スプーラーを使用しているインタ フェースは、 [IMSLogon](imslogoniunknown.md)と[IMsgStore](imsgstoreimapiprop.md)のインターフェイスです。 これらのインタ フェースは通常、メッセージ ・ ストアが最初にログオンしているときに、作成、メッセージの[MSProviderInit](msproviderinit.md)エントリ ポイントの格納が DLL 可能性がありますも作成します。 
  
**IMSLogon**および**IMsgStore**インターフェイスは、いくつかの方法を共有するため、両方のこれらのインターフェイスから継承する 1 つのクラス オブジェクトを作成するより簡単があります。 それぞれ別のオブジェクトでは、これらのインタ フェースを実装し、 **IMSLogon**および**IMsgStore**インタ フェース内のメソッドから呼び出すことができますし、共有メソッドを実装する DLL の内部ヘルパー関数を作成できます。 
  
次の図は、実行中のメッセージ ・ ストア内のオブジェクト階層の上位レベルのアウトラインを示します。
  
**メッセージ ストアのオブジェクト階層**
  
![メッセージ オブジェクトの階層を格納します。](media/storeobj.gif "メッセージ オブジェクトの階層を格納します。")
  
## <a name="see-also"></a>関連項目

- [MAPI ���b�Z�[�W �X�g�A �v���o�C�_�[�̊J��](developing-a-mapi-message-store-provider.md)

