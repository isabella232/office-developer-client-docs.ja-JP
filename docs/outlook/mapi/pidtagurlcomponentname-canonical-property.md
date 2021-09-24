---
title: PidTagUrlComponentName 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.PidTagUrlComponentName
api_type:
- COM
ms.assetid: a21906f9-5408-41ba-a89b-273ab60eeef3
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 99aca12724f7f61e88905dd28c711d2e90f7103d
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59550289"
---
# <a name="pidtagurlcomponentname-canonical-property"></a>PidTagUrlComponentName 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
メッセージの URL コンポーネント名。 
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_URL_COMP_NAME、PR_URL_COMP_NAME_A、PR_URL_COMP_NAME_W  <br/> |
|識別子:  <br/> |0x10F3  <br/> |
|データの種類 :   <br/> |PT_STRING8、PT_UNICODE  <br/> |
|エリア:  <br/> |一般的なメッセージング  <br/> |
   
## <a name="remarks"></a>注釈

これらのプロパティは、フォルダー内で一意である必要があります。 メッセージの作成時に設定しない場合、メッセージ ストアは、メッセージ クラスに応じて、さまざまなメッセージ プロパティに基づいてこれらのプロパティを設定する必要があります。 たとえば **、IPM です。メモ** と **IPM。予定** メッセージには、このプロパティは、PR_SUBJECT **(** [PidTagSubject](pidtagsubject-canonical-property.md)) プロパティと IPM に基づいて **設定されている必要があります。連絡先** メッセージには **、dispidFileUnder** ([PidLidFileUnder](pidlidfileunder-canonical-property.md)) プロパティに基づいてこのプロパティが設定されている必要があります。 他のほとんどのメッセージ クラスでは、このプロパティは、PR_DISPLAY_NAME **(** [PidTagDisplayName](pidtagdisplayname-canonical-property.md)) プロパティに基づく必要があります。
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連するプロトコル仕様へのExchange Server提供します。
    
[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> メッセージ オブジェクトと添付ファイル オブジェクトを処理します。
    
[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)
  
> メッセージオブジェクトと添付ファイル オブジェクトを効率的なストリーム表現にエンコードおよびデコードします。
    
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

