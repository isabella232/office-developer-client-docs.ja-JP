---
title: PidLidTaskMode 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidLidTaskMode
api_type:
- COM
ms.assetid: 185db683-301a-4d91-a583-6959853fa1ad
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 39e6e0f58073a3acafd48864eed18664cfe1d68e
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59630027"
---
# <a name="pidlidtaskmode-canonical-property"></a>PidLidTaskMode 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
タスクの割り当て状態を指定します。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |dispidTaskMode  <br/> |
|プロパティ セット:  <br/> |PSETID_Common  <br/> |
|長い ID (LID):  <br/> |0x00008518  <br/> |
|データの種類 :   <br/> |PT_LONG  <br/> |
|エリア:  <br/> |タスク  <br/> |
   
## <a name="remarks"></a>注釈

値は、次のいずれかを指定する必要があります。
  
|**値**|**説明**|
|:-----|:-----|
|0x00000000  <br/> |タスクが割り当てられていない。  <br/> |
|0x00000001  <br/> |タスクはタスク要求に埋め込まれている。  <br/> |
|0x00000002  <br/> |タスクは、タスクの割り当て先によって受け入れされました。  <br/> |
|0x00000003  <br/> |タスクは、タスクの割り当て先によって拒否されました。  <br/> |
|0x00000004  <br/> |タスクはタスク更新プログラムに埋め込まれている。  <br/> |
|0x00000005  <br/> |タスクがタスク割り当て人に割り当て済みです。  <br/> |
   
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> プロパティ セットの定義と、関連するプロトコル仕様へのExchange Serverを提供します。
    
[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)
  
> タスク、タスクの割り当て、およびタスク更新の電子的な同等物をモデル化する複数のオブジェクトを定義します。
    
### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型の定義を提供します。
    
## <a name="see-also"></a>関連項目



[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名を MAPI 名にマッピングする](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名を標準プロパティ名にマッピングする](mapping-mapi-names-to-canonical-property-names.md)

