---
title: PidTagRpcOverHttpFlags 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: c8b30768-cf83-450d-9fe2-567a5e0c2f57
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: cf1f3b4d72426fb5f80decdc074a622b140657c8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327448"
---
# <a name="pidtagrpcoverhttpflags-canonical-property"></a>PidTagRpcOverHttpFlags 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
ハイパーテキスト転送プロトコル (HTTP) をMicrosoft Office Outlookリモート プロシージャ 呼び出し (RPC) を使用Microsoft Exchange Serverに接続するために使用されるプロファイルの設定が含まれる。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_ROH_FLAGS  <br/> |
|識別子:  <br/> |0x6623  <br/> |
|データの種類 :   <br/> |PT_LONG  <br/> |
|エリア:  <br/> |その他  <br/> |
   
## <a name="remarks"></a>注釈

PR_ROH_FLAGS **プロパティ** は、メッセージング アプリケーション プログラミング インターフェイス (MAPI) プロファイルのグローバル プロファイル セクションに格納されます。 PR_ROH_FLAGSの **値** は、次のフラグの 1 つ以上で構成されるビットマスクです。 
  
|**名前**|**値**|**説明**|
|:-----|:-----|:-----|
|**ROHFLAGS_USE_ROH** <br/> |0x1  <br/> |Connect HTTP を使用してExchange Serverにアクセスします。  <br/> |
|**ROHFLAGS_SSL_ONLY** <br/> |0x2  <br/> |Connectソケット層 (SSL) Exchange Serverを使用してサーバーにアクセスします。  <br/> |
|**ROHFLAGS_MUTUAL_AUTH** <br/> |0x4  <br/> |SSL を使用して接続するときに、セッションを相互に認証します。  <br/> |
|**ROHFLAGS_HTTP_FIRST_ON_FAST** <br/> |0x8  <br/> |高速ネットワークでは、最初に HTTP を使用して接続します。 次に、TCP/IP を使用して接続します。  <br/> |
|**ROHFLAGS_HTTP_FIRST_ON_SLOW** <br/> |0x20  <br/> |低速ネットワークでは、最初に HTTP を使用して接続します。 次に、TCP/IP を使用して接続します。  <br/> |
   
たとえば、HTTP で RPC を有効にし、SSL を要求し、低速接続で最初に HTTP プロトコルを使用する必要がある場合は **、PR_ROH_FLAGS PR_ROH_FLAGS** プロパティの値を **0x23** に設定します。 `ROHFLAGS_USE_ROH | ROHFLAGS_SSL_ONLY | ROHFLAGS_HTTP_FIRST_ON_SLOW` 
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連するプロトコル仕様へのExchange Server提供します。
    
[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> リモート操作で使用される基本的なデータ構造を定義します。
    
[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> 電子メール メッセージ オブジェクトで許容されるプロパティと操作を指定します。
    
### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型の定義を提供します。
    
Mapitags.h
  
> 代替名として一覧表示されるプロパティの定義が含まれる。
    
## <a name="see-also"></a>関連項目



[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名を MAPI 名にマッピングする](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名を標準プロパティ名にマッピングする](mapping-mapi-names-to-canonical-property-names.md)

