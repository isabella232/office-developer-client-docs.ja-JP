---
title: PidLidPercentComplete 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidLidPercentComplete
api_type:
- COM
ms.assetid: e63792b1-9580-4702-a6d7-dd3ae5007a4a
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 870b4e0edb360ac36525f94b0605af930eee8fa3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357975"
---
# <a name="pidlidpercentcomplete-canonical-property"></a>PidLidPercentComplete 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
ユーザーがタスクに対して行った進行状況を示します。 
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |dispidPercentComplete  <br/> |
|プロパティ セット:  <br/> |PSETID_Task  <br/> |
|長い ID (LID):  <br/> |0x00008102  <br/> |
|データの種類 :   <br/> |PT_R8  <br/> |
|エリア:  <br/> |タスク  <br/> |
   
## <a name="remarks"></a>注釈

このプロパティの値は、0.0 以上 1.0 以下の数値である必要があります。1.0 は作業が完了し、0.0 は作業が開始されていないと示します。
  
時間フラグが設定されたメッセージ オブジェクトの場合、オブジェクトにフラグが設定されている場合、このプロパティの値は 1.0 に設定する必要があります。それ以外の場合は 0.0 に設定する必要があります。
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> プロパティ セットの定義と、関連するプロトコル仕様へのExchange Serverを提供します。
    
[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)
  
> タスク、タスクの割り当て、およびタスク更新の電子的な同等物をモデル化する複数のオブジェクトを定義します。
    
[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)
  
> フラグに関連するプロパティと操作を指定します。
    
[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)
  
> インターネット標準の電子メール規則からメッセージ オブジェクトに変換します。
    
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

