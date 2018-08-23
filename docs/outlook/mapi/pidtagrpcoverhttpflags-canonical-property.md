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
ms.openlocfilehash: 151aa730f2ae6a4d39ffa474eb7ecd79ed5602eb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803366"
---
# <a name="pidtagrpcoverhttpflags-canonical-property"></a>PidTagRpcOverHttpFlags 標準プロパティ

  
  
**適用対象**: Outlook 
  
ハイパー テキスト転送プロトコル (HTTP) 経由でリモート プロシージャ コール (RPC) を使用して Microsoft Exchange Server に接続する Microsoft Office Outlook で使用されるプロファイルの設定が含まれています。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_ROH_FLAGS  <br/> |
|識別子:  <br/> |0x6623  <br/> |
|データの種類 :   <br/> |PT_LONG  <br/> |
|領域:  <br/> |その他  <br/> |
   
## <a name="remarks"></a>注釈

**PR_ROH_FLAGS**プロパティは、メッセージング アプリケーション プログラミング インターフェイス (MAPI) プロファイルのグローバル プロファイル セクションに格納されます。 **PR_ROH_FLAGS**の値は、次のフラグの 1 つ以上で構成されるビットマスクです。 
  
|**名前**|**値**|**説明**|
|:-----|:-----|:-----|
|**ROHFLAGS_USE_ROH** <br/> |0x1  <br/> |HTTP 経由で RPC を使用して Exchange Server に接続します。  <br/> |
|**ROHFLAGS_SSL_ONLY** <br/> |0x2  <br/> |セキュア ソケット レイヤー (SSL) のみを使用して Exchange Server に接続します。  <br/> |
|**ROHFLAGS_MUTUAL_AUTH** <br/> |0x4  <br/> |セッションを相互認証で SSL を使用して接続するとき。  <br/> |
|**ROHFLAGS_HTTP_FIRST_ON_FAST** <br/> |0x8  <br/> |高速ネットワークでは、最初に HTTP を使用して接続します。 TCP/IP を使用して接続し、します。  <br/> |
|**ROHFLAGS_HTTP_FIRST_ON_SLOW** <br/> |0x20  <br/> |低速ネットワークでは、最初に HTTP を使用して接続します。 TCP/IP を使用して接続し、します。  <br/> |
   
たとえば、 **PR_ROH_FLAGS**を設定するのにを RPC over HTTP、SSL を要求して、低速接続で HTTP プロトコルを最初に使用することを指定する有効にするプロパティの値を設定、 **PR_ROH_FLAGS**プロパティを`ROHFLAGS_USE_ROH | ROHFLAGS_SSL_ONLY | ROHFLAGS_HTTP_FIRST_ON_SLOW`0x23 に等しいであります。 
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連する Exchange Server プロトコルの仕様への参照を提供します。
    
[[MS OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> リモート操作で使用される基本的なデータ構造を定義します。
    
[[MS OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> プロパティは、電子メール メッセージのオブジェクトに対して許可する操作を指定します。
    
### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型定義を提供します。
    
Mapitags.h
  
> 代替名として記載されているプロパティの定義が含まれています。
    
## <a name="see-also"></a>関連項目



[MAPI プロパティ](mapi-properties.md)
  
[標準の MAPI プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名から MAPI 名へのマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名から標準プロパティ名へのマッピング](mapping-mapi-names-to-canonical-property-names.md)

