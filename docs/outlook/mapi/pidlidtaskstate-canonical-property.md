---
title: PidLidTaskState 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskState
api_type:
- COM
ms.assetid: 06d1f8a3-53e1-4c9a-9703-75de7a11a772
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 149f238ea53e0669f4d95c8e6c2b17a2b5a1c209
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316535"
---
# <a name="pidlidtaskstate-canonical-property"></a>PidLidTaskState 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
タスクの現在の割り当ての状態を示します。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |dispidTaskState  <br/> |
|プロパティ セット:  <br/> |PSETID_Task  <br/> |
|長い ID (LID):  <br/> |0x00008113  <br/> |
|データの種類 :   <br/> |PT_LONG  <br/> |
|エリア:  <br/> |タスク  <br/> |
   
## <a name="remarks"></a>注釈

このプロパティの値は、次のいずれかを指定する必要があります。
  
|**値**|**説明**|
|:-----|:-----|
|0x00000000  <br/> |このタスクは、タスク拒否に埋め込まれたタスクに対応するために作成されましたが、ローカルで見つかりませんでした。  <br/> |
|0x00000001  <br/> |タスクが割り当てられていない。  <br/> |
|0x00000002  <br/> |タスクは、割り当てられたタスクのタスクの割り当て先のコピーです。  <br/> |
|0x00000003  <br/> |タスクは、割り当てられたタスクのタスク割り当て者のコピーです。  <br/> |
|0x00000004  <br/> |タスクは、拒否されたタスクのタスク割り当て者のコピーです。  <br/> |
   
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> プロパティ セットの定義と関連するプロトコル仕様への参照Exchange Server提供します。
    
[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)
  
> タスク、タスクの割り当て、およびタスク更新の電子的な同等物をモデル化する複数のオブジェクトを定義します。
    
[[MS-OXOSFLD]](https://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)
  
> メールボックス内の特別なフォルダーを作成および検索するためのプロパティと操作を指定します。
    
[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)
  
> IETF RFC2445、RFC2446、RFC2447、および予定オブジェクトと会議オブジェクトの間で変換します。
    
[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> クライアントとサーバー間のデータ転送の順序とフローを処理します。
    
### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型の定義を提供します。
    
## <a name="see-also"></a>関連項目



[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名を MAPI 名にマッピングする](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名を標準プロパティ名にマッピングする](mapping-mapi-names-to-canonical-property-names.md)

