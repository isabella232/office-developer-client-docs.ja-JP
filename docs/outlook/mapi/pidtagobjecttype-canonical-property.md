---
title: PidTagObjectType 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagObjectType
api_type:
- HeaderDef
ms.assetid: 37da4ff5-300d-479f-a8b4-6fc36df997d9
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: b433db7cb157afbf8c3b506f2ed95b04b7b88564
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329226"
---
# <a name="pidtagobjecttype-canonical-property"></a>PidTagObjectType 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
オブジェクトの種類を格納します。 
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_OBJECT_TYPE  <br/> |
|識別子:  <br/> |0x0ffe  <br/> |
|データの種類 :   <br/> |PT_LONG  <br/> |
|エリア:  <br/> |共通  <br/> |
   
## <a name="remarks"></a>解説

このプロパティに含まれているオブジェクトの種類は、 **openentry**インターフェイスを介してアクセスできるオブジェクトで利用できるプライマリインターフェイスに対応しています。 通常は、適切な**openentry**メソッドによって返される_lpulobjtype_パラメーターを調べて取得します。 インターフェイスが他の方法で取得された場合は、 [imapiprop:: GetProps](imapiprop-getprops.md)を呼び出してこのプロパティの値を取得します。 
  
このプロパティには、次のいずれかの値を指定できます。
  
MAPI_ABCONT 
  
> アドレス帳のコンテナーオブジェクト 
    
MAPI_ADDRBOOK 
  
> アドレス帳オブジェクト 
    
MAPI_ATTACH 
  
> メッセージ添付オブジェクト 
    
MAPI_DISTLIST 
  
> 配布リストオブジェクト 
    
MAPI_FOLDER 
  
> フォルダー オブジェクト 
    
MAPI_FORMINFO 
  
> Form オブジェクト 
    
MAPI_MAILUSER 
  
> メッセージングユーザーオブジェクト 
    
MAPI_MESSAGE 
  
> Message オブジェクト 
    
MAPI_PROFSECT 
  
> Profile section オブジェクト 
    
MAPI_SESSION 
  
> Session オブジェクト 
    
MAPI_STATUS 
  
> Status オブジェクト 
    
MAPI_STORE 
  
> メッセージストアオブジェクト
    
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連する Exchange Server プロトコル仕様への参照を提供します。
    
[[OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)
  
> ユーザー、連絡先、グループ、およびリソースのリストのプロパティと操作を指定します。
    
[[MS-CHAP]](https://msdn.microsoft.com/library/6dd0a3ea-b4d4-4a73-a857-add03a89a543%28Office.15%29.aspx)
  
> ネームサービスプロバイダインターフェイス (NSPI) サーバーとのクライアントの通信を処理します。
    
[[OXCFOLD]](https://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)
  
> フォルダー操作を処理します。
    
[[OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> クライアントとサーバー間のデータ転送の順序と流れを処理します。
    
[[OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)
  
> インターネット標準の電子メールの規則からメッセージオブジェクトに変換します。
    
[[OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> メッセージと添付ファイルオブジェクトを処理します。
    
[[OXOAB]](https://msdn.microsoft.com/library/b4750386-66ec-4e69-abb6-208dd131c7de%28Office.15%29.aspx)
  
> ローカルアドレス帳のオブジェクトキャッシュのオフラインアドレス帳 (OAB) ファイル形式を指定します。
    
[[OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> 電子メールメッセージオブジェクトに対して許容されるプロパティと操作を指定します。
    
[[OXOSRCH]](https://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)
  
> 検索フォルダーリストの構成を操作するためのプロパティと操作を指定します。
    
### <a name="header-files"></a>ヘッダーファイル

mapidefs.h
  
> データ型定義を提供します。
    
Mapitags
  
> 関連するプロパティとしてリストされているプロパティの定義が含まれます。
    
## <a name="see-also"></a>関連項目



[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名から MAPI 名へのマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名から標準プロパティ名へのマッピング](mapping-mapi-names-to-canonical-property-names.md)

