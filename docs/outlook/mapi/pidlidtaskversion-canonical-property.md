---
title: PidLidTaskVersion 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskVersion
api_type:
- COM
ms.assetid: 3ab77f25-ad11-4501-8d35-ef560c07e2f2
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 3daf8a04afc9cf47d808b46f2cee010e15a33cf9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356494"
---
# <a name="pidlidtaskversion-canonical-property"></a>PidLidTaskVersion 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
タスクの最新の更新プログラムであるコピーを示します。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |dispidTaskVersion  <br/> |
|プロパティ セット:  <br/> |PSETID_Task  <br/> |
|長い ID (LID):  <br/> |0x00008112  <br/> |
|データの種類 :   <br/> |PT_LONG  <br/> |
|エリア:  <br/> |タスク  <br/> |
   
## <a name="remarks"></a>注釈

タスクよりもバージョンが低い更新プログラムは無視されます。 
  
タスク通信にタスクを埋め込む場合、クライアントはタスク通信にも埋め込みタスクの現在のバージョンを設定します。
  
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

