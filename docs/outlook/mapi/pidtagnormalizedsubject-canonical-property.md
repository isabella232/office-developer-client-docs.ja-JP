---
title: PidTagNormalizedSubject 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagNormalizedSubject
api_type:
- HeaderDef
ms.assetid: 2000e6e8-d908-4814-8093-28f8011250c8
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 0f7765fb7898ed76dd7b537bc0eeefc21e626fb4
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59555280"
---
# <a name="pidtagnormalizedsubject-canonical-property"></a>PidTagNormalizedSubject 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
プレフィックスが削除されたメッセージの件名が含まれる。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_NORMALIZED_SUBJECT、PR_NORMALIZED_SUBJECT_A、PR_NORMALIZED_SUBJECT_W  <br/> |
|識別子:  <br/> |0x0E1D  <br/> |
|データの種類 :   <br/> |PT_STRING8、PT_UNICODE  <br/> |
|エリア:  <br/> |メール  <br/> |
   
## <a name="remarks"></a>注釈

これらのプロパティは **、PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)) プロパティおよび **PR_SUBJECT_PREFIX** ([PidTagSubjectPrefix](pidtagsubjectprefix-canonical-property.md)) プロパティのメッセージ ストアまたはトランスポート プロバイダーによって次のように計算されます。
  
- PR_SUBJECT_PREFIXが存在 **し****、PR_SUBJECT** の初期部分文字列である場合 **、PR_NORMALIZED_SUBJECT** と関連付けられたプロパティは、プレフィックスが削除された PR_SUBJECT の内容 **に** 設定されます。 
    
- **PR_SUBJECT_PREFIX** が存在するが、PR_SUBJECT の初期部分文字列ではない場合、PR_SUBJECT_PREFIX は次のルールを使用して PR_SUBJECT から削除および再計算されます。PR_SUBJECT に含まれる文字列が 1 ~ **3** 文字の非数値文字の後にコロンとスペースが続く場合は、コロンとブランクと共に文字列がプレフィックスになります。  数字、空白文字、句読点文字は、有効なプレフィックス文字ではありません。 
    
- この **PR_SUBJECT_PREFIX** が存在しない場合は、前の手順で **PR_SUBJECTを使用** して計算されます。 このプロパティは、プレフィックスが削除されたPR_SUBJECT **の内容** に設定されます。 
    
 **メモ** 指定 **PR_SUBJECT_PREFIX** 文字列の場合、PR_SUBJECT **プロパティは** 同じです。 
  
最終的には、このプロパティはプレフィックスの **後PR_SUBJECT部分** である必要があります。 プレフィックスがない場合、このプロパティは次のプロパティと **同PR_SUBJECT。**
  
 **PR_SUBJECT_PREFIX** このプロパティは [、IMAPIProp::SaveChanges](imapiprop-savechanges.md) 実装の一部として計算する必要があります。 クライアント アプリケーションは [、IMAPIProp::SaveChanges](imapiprop-getprops.md) 呼び出しによってコミットされるまで **、IMAPIProp::GetProps** メソッドの値を求める必要があります。 
  
件名プロパティは、通常、256 文字未満の小さな文字列であり、メッセージ ストア プロバイダーは、オブジェクト リンクおよび埋め込み (OLE) **IStream** インターフェイスをサポートする義務はありません。 クライアントは、必ず最初に **IMAPIProp** インターフェイスを介してアクセスを試行し **、IStream** にアクセスMAPI_E_NOT_ENOUGH_MEMORY必要があります。 
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連するプロトコル仕様へのExchange Server提供します。
    
[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> メッセージ オブジェクトと添付ファイル オブジェクトを処理します。
    
[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)
  
> 連絡先と個人用配布リストで許容されるプロパティと操作を指定します。
    
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

