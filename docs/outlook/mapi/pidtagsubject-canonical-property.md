---
title: PidTagSubject 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagSubject
api_type:
- COM
ms.assetid: aa7ba4d9-c5e0-4ce7-a34e-65f675223bc9
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 0cf9e9f8c10f8d27bd174b8b6f2bf19812dc269d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339257"
---
# <a name="pidtagsubject-canonical-property"></a>PidTagSubject 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
メッセージの完全な件名を含む。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_SUBJECT、PR_SUBJECT_A、PR_SUBJECT_W  <br/> |
|識別子:  <br/> |0x0037  <br/> |
|データの種類 :   <br/> |PT_STRING8、PT_UNICODE  <br/> |
|エリア:  <br/> |一般的なメッセージング  <br/> |
   
## <a name="remarks"></a>注釈

これらのプロパティは、すべてのメッセージ オブジェクトで推奨されます。 
  
これらのプロパティは、常に完全な件名テキスト、つまりプレフィックスと正規化された件名の連結です。 プレフィックスがない場合、正規化された件名は件名と同じになる必要があります。 メッセージ ストアまたはトランスポート プロバイダーは、これらのプロパティと **PR_SUBJECT_PREFIX** ([PidTagSubjectPrefix)](pidtagsubjectprefix-canonical-property.md)プロパティの両方を使用して **、PR_NORMALIZED_SUBJECT** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md)) で説明されているルールを使用して正規化されたサブジェクトを計算します。
  
件名のプロパティは、通常、256 文字未満の小さな文字列であり、メッセージ ストア プロバイダーは **、IStream** インターフェイスをサポートする義務はありません。 クライアントは、必ず最初に **IMAPIProp** インターフェイスを介してアクセスを試行し、IStream にアクセスMAPI_E_NOT_ENOUGH_MEMORY必要があります。   
  
レポートの場合、このプロパティには、元のメッセージの件名の前に、メッセージに何が起こったかを示す文字列が含まれます。
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連するプロトコル仕様へのExchange Server提供します。
    
[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> メッセージ オブジェクトと添付ファイル オブジェクトを処理します。
    
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

