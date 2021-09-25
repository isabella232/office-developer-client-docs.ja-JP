---
title: PidLidContactItemData 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidLidContactItemData
api_type:
- COM
ms.assetid: 411e8f81-c2b9-440a-9e9a-d6add5e4be63
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: f1353f12c7faf067ff983cf1a559796a3b85c72c
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59575191"
---
# <a name="pidlidcontactitemdata-canonical-property"></a>PidLidContactItemData 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
連絡先情報を表示するために使用します。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |dispidContactItemData  <br/> |
|プロパティ セット:  <br/> |PSETID_Address  <br/> |
|長い ID (LID):  <br/> |0x00008007  <br/> |
|データの種類 :   <br/> |PT_MV_LONG  <br/> |
|エリア:  <br/> |Contact  <br/> |
   
## <a name="remarks"></a>注釈

存在する場合、プロパティには 6 つのエントリが必要です。各エントリは、アプリケーションのユーザー インターフェイスの表示フィールドに対応します。
  
|**複数値プロパティへの 1 ベースのインデックス**|**値は、次のいずれかを指定する必要があります。**|**説明**|
|:-----|:-----|:-----|
|1  <br/> |0x00000001  <br/> |アプリケーションは連絡先のホーム アドレスを表示する必要があります。  <br/> |
|1  <br/> |0x00000002または0x00000000  <br/> |アプリケーションは連絡先の作業時間を表示する必要があります。  <br/> |
|1  <br/> |0x00000003  <br/> |アプリケーションは連絡先の他のアドレスを表示する必要があります。  <br/> |
|2  <br/> |0x00008080  <br/> |アプリケーションは Email1 を表示する必要があります。  <br/> |
|2  <br/> |0x00008090  <br/> |アプリケーションは Email2 を表示する必要があります。  <br/> |
|2  <br/> |0x000080A0  <br/> |アプリケーションは Email3 を表示する必要があります。  <br/> |
|3,4,5,6  <br/> |[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)で指定されている電話プロパティまたは FAX 番号の PropertyID。  <br/> |アプリケーションは、対応するプロパティを表示する必要があります。  <br/> |
   
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> プロパティ セットの定義と、関連するプロトコル仕様へのExchange Serverを提供します。
    
[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)
  
> 連絡先と個人用配布リストで許容されるプロパティと操作を指定します。
    
### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型の定義を提供します。
    
## <a name="see-also"></a>関連項目



[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名を MAPI 名にマッピングする](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名を標準プロパティ名にマッピングする](mapping-mapi-names-to-canonical-property-names.md)

