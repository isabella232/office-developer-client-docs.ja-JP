---
title: PidTagRpcOverHttpFlags 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: c8b30768-cf83-450d-9fe2-567a5e0c2f57
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: cf1f3b4d72426fb5f80decdc074a622b140657c8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327448"
---
# <a name="pidtagrpcoverhttpflags-canonical-property"></a>PidTagRpcOverHttpFlags 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
microsoft Office Outlook で、ハイパーテキスト転送プロトコル (HTTP) 経由のリモートプロシージャコール (RPC) を使用して microsoft Exchange Server に接続するために使用されるプロファイルの設定が含まれています。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_ROH_FLAGS  <br/> |
|識別子:  <br/> |0x6623  <br/> |
|データの種類 :   <br/> |PT_LONG  <br/> |
|エリア:  <br/> |その他  <br/> |
   
## <a name="remarks"></a>解説

**PR_ROH_FLAGS**プロパティは、メッセージングアプリケーションプログラミングインターフェイス (MAPI) プロファイルの [グローバルプロファイル] セクションに格納されます。 **PR_ROH_FLAGS**の値は、次の1つ以上のフラグで構成されるビットマスクです。 
  
|**名前**|**値**|**説明**|
|:-----|:-----|:-----|
|**ROHFLAGS_USE_ROH** <br/> |0x1  <br/> |RPC over HTTP を使用して Exchange サーバーに接続します。  <br/> |
|**ROHFLAGS_SSL_ONLY** <br/> |0x2  <br/> |Secure Socket Layer (SSL) のみを使用して Exchange サーバーに接続します。  <br/> |
|**ROHFLAGS_MUTUAL_AUTH** <br/> |0x4  <br/> |SSL を使用して接続しているときにセッションを相互認証します。  <br/> |
|**ROHFLAGS_HTTP_FIRST_ON_FAST** <br/> |0x8  <br/> |高速のネットワークでは、最初に HTTP を使用して接続します。 次に、tcp/ip を使用して接続します。  <br/> |
|**ROHFLAGS_HTTP_FIRST_ON_SLOW** <br/> |0x20  <br/> |低速のネットワークでは、最初に HTTP を使用して接続します。 次に、tcp/ip を使用して接続します。  <br/> |
   
たとえば、 **PR_ROH_FLAGS**プロパティを設定して RPC over HTTP を有効にし、SSL を要求し、最初に低速接続で http プロトコルを使用するように指定するには、 **PR_ROH_FLAGS**プロパティ`ROHFLAGS_USE_ROH | ROHFLAGS_SSL_ONLY | ROHFLAGS_HTTP_FIRST_ON_SLOW`の値を0x23 と等しくなるように設定します。 
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連する Exchange Server プロトコル仕様への参照を提供します。
    
[[OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> リモート操作で使用される基本データ構造を定義します。
    
[[OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> 電子メールメッセージオブジェクトに対して許容されるプロパティと操作を指定します。
    
### <a name="header-files"></a>ヘッダーファイル

mapidefs.h
  
> データ型定義を提供します。
    
Mapitags
  
> 代替名としてリストされているプロパティの定義が含まれています。
    
## <a name="see-also"></a>関連項目



[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名から MAPI 名へのマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名から標準プロパティ名へのマッピング](mapping-mapi-names-to-canonical-property-names.md)

