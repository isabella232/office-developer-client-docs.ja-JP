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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 0cf9e9f8c10f8d27bd174b8b6f2bf19812dc269d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339257"
---
# <a name="pidtagsubject-canonical-property"></a>PidTagSubject 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
メッセージの完全な件名を含みます。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_SUBJECT、PR_SUBJECT_A、PR_SUBJECT_W  <br/> |
|識別子:  <br/> |0x0037  <br/> |
|データの種類 :   <br/> |PT_STRING8、PT_UNICODE  <br/> |
|エリア:  <br/> |一般的なメッセージング  <br/> |
   
## <a name="remarks"></a>解説

これらのプロパティは、すべてのメッセージオブジェクトで推奨されます。 
  
これらのプロパティは常に、完全な件名のテキスト (プレフィックスと正規化された件名の連結) です。 プレフィックスがない場合は、正規化された件名を件名と同じにする必要があります。 メッセージストアまたはトランスポートプロバイダーは、これらのプロパティと**PR_SUBJECT_PREFIX** ([PidTagSubjectPrefix](pidtagsubjectprefix-canonical-property.md)) プロパティの両方を使用して、 **PR_NORMALIZED_SUBJECT**に記述されている規則を使用して正規化されたサブジェクトを計算します ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md))
  
件名のプロパティは通常、256文字未満の小さな文字列で、メッセージストアプロバイダーは、それらの**IStream**インターフェイスをサポートする義務がありません。 クライアントは、常に**imapiprop**インターフェイスを使用してアクセスを試行し、 **MAPI_E_NOT_ENOUGH_MEMORY**が返された場合にのみ**IStream**に頼る必要があります。 
  
レポートの場合、このプロパティには、メッセージに対して発生したことを示す文字列が前にある、元のメッセージの件名が含まれます。
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連する Exchange Server プロトコル仕様への参照を提供します。
    
[[OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> メッセージと添付ファイルオブジェクトを処理します。
    
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

