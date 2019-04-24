---
title: PidTagAttachPayloadProviderGuidString 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachPayloadProviderGuidString
api_type:
- HeaderDef
ms.assetid: c9d4b561-53b3-492b-9324-9376dd7abddf
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 5051784ea08316477f3c8888ada9170e3d99c2b5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32361104"
---
# <a name="pidtagattachpayloadproviderguidstring-canonical-property"></a>PidTagAttachPayloadProviderGuidString 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
MIME X ペイロードプロバイダーの Guid ヘッダーフィールドの値を格納します。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_ATTACH_PAYLOAD_PROV_GUID_STR、PR_ATTACH_PAYLOAD_PROV_GUID_STR_A、PR_ATTACH_PAYLOAD_PROV_GUID_STR_W  <br/> |
|識別子:  <br/> |0x3719  <br/> |
|データの種類 :   <br/> |PT_STRING8、PT_UNICODE  <br/> |
|エリア:  <br/> |Outlook アプリケーション  <br/> |
   
## <a name="remarks"></a>解説

これらのプロパティの値を設定するには、mime クライアントは、添付ファイルとして分析される mime エンティティに、X ペイロードプロバイダー-Guid ヘッダーフィールドを書き込む必要があります。
  
MIME リーダーは、このヘッダーフィールド値を対応するプロパティの値にコピーする必要があります。 mime リーダーは、添付ファイルとしてではなく、メッセージまたはメッセージ本文として分析される mime エンティティに表示される場合、このヘッダーフィールドを無視する必要があります。
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連する Exchange Server プロトコル仕様への参照を提供します。
    
[[OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)
  
> インターネット標準の電子メールの規則からメッセージオブジェクトに変換します。
    
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

