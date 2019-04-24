---
title: PidLidContactItemData 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidContactItemData
api_type:
- COM
ms.assetid: 411e8f81-c2b9-440a-9e9a-d6add5e4be63
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 031e5483539ce17c8b9b994690985c2349573e27
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32319511"
---
# <a name="pidlidcontactitemdata-canonical-property"></a>PidLidContactItemData 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
連絡先情報を表示するために使用されます。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |dispidContactItemData  <br/> |
|プロパティセット:  <br/> |PSETID_Address  <br/> |
|ロング ID (LID):  <br/> |0x00008007  <br/> |
|データの種類 :   <br/> |PT_MV_LONG  <br/> |
|エリア:  <br/> |連絡先  <br/> |
   
## <a name="remarks"></a>解説

指定する場合、プロパティには、アプリケーションのユーザーインターフェイスで表示されるフィールドに対応する6つのエントリが必要です。
  
|**複数値を持つプロパティへの1から始まるインデックス**|**この値は、次のいずれかであることが必要です。**|**説明**|
|:-----|:-----|:-----|
|1-d  <br/> |0x00000001  <br/> |アプリケーションには、連絡先の自宅の住所が表示されます。  <br/> |
|1-d  <br/> |0x00000002 または0x00000000  <br/> |アプリケーションに連絡先の仕事が表示されます。  <br/> |
|1-d  <br/> |0x00000003  <br/> |アプリケーションには、連絡先のその他のアドレスが表示されます。  <br/> |
|pbm-2  <br/> |0x00008080  <br/> |アプリケーションに Email1 が表示されます。  <br/> |
|pbm-2  <br/> |0x00008090  <br/> |アプリケーションに Email2 が表示されます。  <br/> |
|pbm-2  <br/> |0x000080a0  <br/> |アプリケーションに Email3 が表示されます。  <br/> |
|3、4、5、6  <br/> |PropertyID [[OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)で指定されている電話のプロパティまたは fax 番号のいずれかを指定します。  <br/> |アプリケーションには、対応するプロパティが表示されます。  <br/> |
   
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> プロパティセットの定義と、関連する Exchange Server プロトコルの仕様への参照を提供します。
    
[[OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)
  
> 連絡先および個人用配布リストに対して許容されるプロパティと操作を指定します。
    
### <a name="header-files"></a>ヘッダーファイル

mapidefs.h
  
> データ型定義を提供します。
    
## <a name="see-also"></a>関連項目



[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名から MAPI 名へのマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名から標準プロパティ名へのマッピング](mapping-mapi-names-to-canonical-property-names.md)

