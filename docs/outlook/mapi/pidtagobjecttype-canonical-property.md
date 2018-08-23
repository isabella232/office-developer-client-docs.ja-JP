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
ms.openlocfilehash: 2830da6aad561045a7ecdd953286c90edea88ca2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803030"
---
# <a name="pidtagobjecttype-canonical-property"></a>PidTagObjectType 標準プロパティ

  
  
**適用対象**: Outlook 
  
オブジェクトの種類が含まれています。 
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_OBJECT_TYPE  <br/> |
|識別子:  <br/> |0x0FFE  <br/> |
|データの種類 :   <br/> |PT_LONG  <br/> |
|領域:  <br/> |Common  <br/> |
   
## <a name="remarks"></a>注釈

**OpenEntry**インタ フェースを介してアクセス可能なオブジェクトで使用できる主要なインターフェイスに、このプロパティに含まれているオブジェクトの種類に対応しています。 通常は、適切な**OpenEntry**メソッドによって返される_lpulObjType_パラメーターを参照して取得されます。 インタ フェースの他の方法で取得するときは、このプロパティの値を取得する[IMAPIProp::GetProps](imapiprop-getprops.md)を呼び出します。 
  
このプロパティは、次の値の 1 つだけ持つことができます。
  
MAPI_ABCONT 
  
> アドレス帳コンテナー オブジェクト 
    
MAPI_ADDRBOOK 
  
> アドレス帳オブジェクト 
    
MAPI_ATTACH 
  
> メッセージの添付ファイルのオブジェクト 
    
MAPI_DISTLIST 
  
> 配布リスト オブジェクト 
    
MAPI_FOLDER 
  
> フォルダー オブジェクト 
    
MAPI_FORMINFO 
  
> フォーム オブジェクト 
    
MAPI_MAILUSER 
  
> メッセージングのユーザー オブジェクト 
    
MAPI_MESSAGE 
  
> Message オブジェクト 
    
MAPI_PROFSECT 
  
> プロファイル セクションのオブジェクト 
    
MAPI_SESSION 
  
> セッション オブジェクト 
    
MAPI_STATUS 
  
> ステータス オブジェクト 
    
MAPI_STORE 
  
> メッセージ ストアのオブジェクト
    
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連する Exchange Server プロトコルの仕様への参照を提供します。
    
[[MS OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)
  
> プロパティとユーザー、連絡先、グループ、およびリソースのリストの操作を指定します。
    
[[MS NSPI]](http://msdn.microsoft.com/library/6dd0a3ea-b4d4-4a73-a857-add03a89a543%28Office.15%29.aspx)
  
> ネーム サービス プロバイダー インターフェイス (NSPI) サーバーとクライアントの通信を処理します。
    
[[MS OXCFOLD]](http://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)
  
> フォルダーの操作を処理します。
    
[[MS OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> 順序と、クライアントとサーバー間のデータ転送のフローを処理します。
    
[[MS OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)
  
> メッセージ オブジェクト インターネット標準の電子メールの表記規則からに変換します。
    
[[MS OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> メッセージと添付ファイルのオブジェクトを処理します。
    
[[MS OXOAB]](http://msdn.microsoft.com/library/b4750386-66ec-4e69-abb6-208dd131c7de%28Office.15%29.aspx)
  
> ローカル アドレス帳のオブジェクト キャッシュのオフライン アドレス帳 (OAB) ファイル形式を指定します。
    
[[MS OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> プロパティは、電子メール メッセージのオブジェクトに対して許可する操作を指定します。
    
[[MS OXOSRCH]](http://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)
  
> プロパティや検索フォルダーの一覧の構成を操作するための動作を指定します。
    
### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型定義を提供します。
    
Mapitags.h
  
> 関連付けられているプロパティとして記載されているプロパティの定義が含まれています。
    
## <a name="see-also"></a>関連項目



[MAPI プロパティ](mapi-properties.md)
  
[標準の MAPI プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名から MAPI 名へのマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名から標準プロパティ名へのマッピング](mapping-mapi-names-to-canonical-property-names.md)

