---
title: PidTagContainerClass 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagContainerClass
api_type:
- HeaderDef
ms.assetid: db249e9e-f1f0-4b95-8cd9-daa7c53ddb32
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 423e5d5cbb2cd66f4bd47c76ef93998420072593
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59571102"
---
# <a name="pidtagcontainerclass-canonical-property"></a>PidTagContainerClass 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
フォルダーの種類を説明するテキスト文字列が含まれます。 このプロパティは一般に無視されます。Microsoft® Exchange Server 2003 メールボックス マネージャー Exchange Server前のバージョンでは、このプロパティが存在すると予想されます。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_CONTAINER_CLASS、PR_CONTAINER_CLASS_A、PR_CONTAINER_CLASS_W  <br/> |
|識別子:  <br/> |0x3613  <br/> |
|データの種類 :   <br/> |PT_STRING8、PT_UNICODE  <br/> |
|エリア:  <br/> |コンテナー  <br/> |
   
## <a name="remarks"></a>注釈

これらのプロパティは、通常、ユーザーが使用Exchange Server。 ただし、Microsoft Office Outlook®フォルダーに添付します。 さらに、2003 メールボックス マネージャー Exchange Server以前Exchange Serverのバージョンでは、これらのプロパティを持つフォルダーが正しく処理されない場合があります。
  
これらのプロパティには、次の表の文字列値を割り当てることができます。
  
|**値**|**フォルダーの内容**|
|:-----|:-----|
|IPF.Appointment  <br/> |予定  <br/> |
|IPF.Contact  <br/> |連絡先  <br/> |
|IPF。ジャーナル  <br/> |Outlookジャーナル エントリ  <br/> |
|IPF.Note  <br/> |メール メッセージとメモ  <br/> |
|IPF。StickyNote  <br/> |Outlook 付箋  <br/> |
|IPF.Task  <br/> |Outlook の仕事  <br/> |
   
メール メッセージを含むフォルダーの場合、これらのプロパティは IPF に設定する必要があります。注。
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連するプロトコル仕様へのExchange Server提供します。
    
[[MS-OXOSFLD]](https://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)
  
> メールボックス内の特別なフォルダーを作成および検索するためのプロパティと操作を指定します。
    
[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> 予定、会議出席依頼、および応答メッセージのプロパティと操作を指定します。
    
[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)
  
> 連絡先および個人用配布リスト オブジェクトに対して許容されるプロパティと操作を指定します。
    
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

