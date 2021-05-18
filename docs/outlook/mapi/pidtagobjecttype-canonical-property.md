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
description: '最終更新日: 2015 年 3 月 9 日'
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
|識別子:  <br/> |0x0FFE  <br/> |
|データの種類 :   <br/> |PT_LONG  <br/> |
|エリア:  <br/> |共通  <br/> |
   
## <a name="remarks"></a>注釈

このプロパティに含まれるオブジェクトの種類は **、OpenEntry** インターフェイスからアクセスできるオブジェクトで使用できるプライマリ インターフェイスに対応します。 通常は、適切な OpenEntry メソッドによって返される  _lpulObjType_ パラメーターを **参照して取得** します。 インターフェイスが他の方法で取得された場合は [、IMAPIProp::GetProps](imapiprop-getprops.md) を呼び出して、このプロパティの値を取得します。 
  
このプロパティには、次のいずれかの値を指定できます。
  
MAPI_ABCONT 
  
> アドレス帳コンテナー オブジェクト 
    
MAPI_ADDRBOOK 
  
> アドレス帳オブジェクト 
    
MAPI_ATTACH 
  
> メッセージ添付オブジェクト 
    
MAPI_DISTLIST 
  
> 配布リスト オブジェクト 
    
MAPI_FOLDER 
  
> フォルダー オブジェクト 
    
MAPI_FORMINFO 
  
> Form オブジェクト 
    
MAPI_MAILUSER 
  
> メッセージング ユーザー オブジェクト 
    
MAPI_MESSAGE 
  
> Message オブジェクト 
    
MAPI_PROFSECT 
  
> Profile section オブジェクト 
    
MAPI_SESSION 
  
> Session オブジェクト 
    
MAPI_STATUS 
  
> Status オブジェクト 
    
MAPI_STORE 
  
> メッセージ ストア オブジェクト
    
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連するプロトコル仕様へのExchange Server提供します。
    
[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)
  
> ユーザー、連絡先、グループ、およびリソースの一覧のプロパティと操作を指定します。
    
[[MS-NSPI]](https://msdn.microsoft.com/library/6dd0a3ea-b4d4-4a73-a857-add03a89a543%28Office.15%29.aspx)
  
> ネーム サービス プロバイダー インターフェイス (NSPI) サーバーとのクライアントの通信を処理します。
    
[[MS-OXCFOLD]](https://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)
  
> フォルダー操作を処理します。
    
[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> クライアントとサーバー間のデータ転送の順序とフローを処理します。
    
[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)
  
> インターネット標準の電子メール規則からメッセージ オブジェクトに変換します。
    
[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> メッセージ オブジェクトと添付ファイル オブジェクトを処理します。
    
[[MS-OXOAB]](https://msdn.microsoft.com/library/b4750386-66ec-4e69-abb6-208dd131c7de%28Office.15%29.aspx)
  
> ローカル アドレス帳オブジェクト キャッシュのオフライン アドレス帳 (OAB) ファイル形式を指定します。
    
[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> 電子メール メッセージ オブジェクトで許容されるプロパティと操作を指定します。
    
[[MS-OXOSRCH]](https://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)
  
> 検索フォルダー 一覧の構成を操作するためのプロパティと操作を指定します。
    
### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型の定義を提供します。
    
Mapitags.h
  
> 関連付けられたプロパティとして一覧表示されるプロパティの定義が含まれる。
    
## <a name="see-also"></a>関連項目



[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名を MAPI 名にマッピングする](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名を標準プロパティ名にマッピングする](mapping-mapi-names-to-canonical-property-names.md)

