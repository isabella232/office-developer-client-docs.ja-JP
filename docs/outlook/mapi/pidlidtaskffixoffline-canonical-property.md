---
title: PidLidTaskFFixOffline 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskFFixOffline
api_type:
- COM
ms.assetid: bbaf7df4-2de0-4da3-9125-eb24dfa94cd8
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 226e59ef6aa88bc290cf5aeb4d620979f926e1eb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303039"
---
# <a name="pidlidtaskffixoffline-canonical-property"></a>PidLidTaskFFixOffline 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
**dispidTaskOwner** ([PidLidTaskOwner](pidlidtaskowner-canonical-property.md)) プロパティの精度を示します。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |dispidTaskFFixOffline  <br/> |
|プロパティ セット:  <br/> |PSETID_Task  <br/> |
|長い ID (LID):  <br/> |0x0000812C  <br/> |
|データの種類 :   <br/> |PT_BOOLEAN  <br/> |
|エリア:  <br/> |タスク  <br/> |
   
## <a name="remarks"></a>注釈

**dispidTaskFFixOffline** プロパティが FALSE に設定されている場合、または設定されていない場合 **、dispidTaskOwner** プロパティの値は正しいです。 **dispidTaskFFixOffline** が TRUE に設定されている場合、クライアントは **dispidTaskOwner** の正確な値を判断できません。 その場合、クライアントは **dispidTaskOwner** を "不明" などの一般的な所有者名に設定できます。 ただし、クライアントで **dispidTaskFFixOffline** 値が TRUE に検出され、正確な所有者名を特定できる場合、クライアントは **dispidTaskOwner を更新し、dispidTaskFFixOffline** を FALSE に設定する必要があります。  
  
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

