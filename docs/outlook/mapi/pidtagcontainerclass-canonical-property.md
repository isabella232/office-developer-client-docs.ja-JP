---
title: PidTagContainerClass 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagContainerClass
api_type:
- HeaderDef
ms.assetid: db249e9e-f1f0-4b95-8cd9-daa7c53ddb32
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: c5b80831607f473208ce987a720c7e80e44b6d80
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32283150"
---
# <a name="pidtagcontainerclass-canonical-property"></a>PidTagContainerClass 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
フォルダーの種類を説明するテキスト文字列を格納します。 このプロパティは通常は無視されますが、exchange server 2003 メールボックスマネージャーより前のバージョンの Microsoft ® exchange server は、このプロパティが存在することを前提としています。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_CONTAINER_CLASS、PR_CONTAINER_CLASS_A、PR_CONTAINER_CLASS_W  <br/> |
|識別子:  <br/> |0x3613  <br/> |
|データの種類 :   <br/> |PT_STRING8、PT_UNICODE  <br/> |
|エリア:  <br/> |Container  <br/> |
   
## <a name="remarks"></a>解説

これらのプロパティは、Exchange Server では通常使用されません。 ただし、Microsoft Office Outlook ®はそれらをメールボックスフォルダーに添付します。 また、exchange server 2003 メールボックスマネージャーより前のバージョンの exchange server は、これらのプロパティを持たないフォルダーを誤って処理することがあります。
  
これらのプロパティには、次の表の文字列値を割り当てることができます。
  
|**値**|**フォルダーの内容**|
|:-----|:-----|
|IPF.Appointment  <br/> |予定  <br/> |
|IPF.Contact  <br/> |連絡先  <br/> |
|.ipf.雑誌  <br/> |Outlook の履歴項目  <br/> |
|IPF.Note  <br/> |メールメッセージとメモ  <br/> |
|.ipf.ipm.stickynote  <br/> |Outlook 付箋  <br/> |
|IPF.Task  <br/> |Outlook の仕事  <br/> |
   
メールメッセージを含むフォルダーの場合は、これらのプロパティを IPF に設定する必要があります。こと.
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連する Exchange Server プロトコル仕様への参照を提供します。
    
[[OXOSFLD]](https://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)
  
> メールボックス内の特別なフォルダーを作成および検索するためのプロパティと操作を指定します。
    
[[OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> 予定、会議出席依頼、および応答メッセージのプロパティと操作を指定します。
    
[[OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)
  
> 連絡先および個人用配布リストオブジェクトに対して許容されるプロパティと操作を指定します。
    
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

