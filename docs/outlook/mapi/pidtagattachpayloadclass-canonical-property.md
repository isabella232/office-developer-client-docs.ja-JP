---
title: PidTagAttachPayloadClass 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachPayloadClass
api_type:
- HeaderDef
ms.assetid: bc4de217-8241-45e7-9e97-8f0c1b16691a
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: d00c1823ba152c20be213f16fe4e3ea3c771a83a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22574322"
---
# <a name="pidtagattachpayloadclass-canonical-property"></a>PidTagAttachPayloadClass 標準プロパティ

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
MIME X ・ ペイロード ・ クラスのヘッダー フィールドの値が含まれています。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_ATTACH_PAYLOAD_CLASS、PR_ATTACH_PAYLOAD_CLASS_A、PR_ATTACH_PAYLOAD_CLASS_W  <br/> |
|識別子:  <br/> |0x371A  <br/> |
|データの種類 :   <br/> |PT_STRING8、PT_UNICODE  <br/> |
|領域:  <br/> |Outlook アプリケーション  <br/> |
   
## <a name="remarks"></a>注釈

これらのプロパティの値を設定するのには MIME クライアントは、添付ファイルとして解析される MIME エンティティに X ・ ペイロード ・ クラスのヘッダー フィールドを記述する必要があります。
  
MIME のリーダーでは、このヘッダー フィールドの値を対応するプロパティの値にコピーする必要があります。 MIME のリーダーは、添付ファイルとしてではなく、メッセージまたはメッセージの本文として分析する MIME エンティティ上に表示されるとき、このヘッダー フィールドを無視してください。
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連する Exchange Server プロトコルの仕様への参照を提供します。
    
[[MS OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)
  
> メッセージ オブジェクト インターネット標準の電子メールの表記規則からに変換します。
    
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

