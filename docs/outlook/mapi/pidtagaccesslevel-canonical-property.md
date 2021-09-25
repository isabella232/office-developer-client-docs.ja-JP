---
title: PidTagAccessLevel 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagAccessLevel
api_type:
- HeaderDef
ms.assetid: 8f7119c7-ffc3-47cf-aa1b-b4e56bcc5a24
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: ba27e5669deb5fe5433ff69a1f6361965404bba3
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59595337"
---
# <a name="pidtagaccesslevel-canonical-property"></a>PidTagAccessLevel 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
オブジェクトへのクライアントのアクセス レベルを示します。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_ACCESS_LEVEL  <br/> |
|識別子:  <br/> |0x0FF7  <br/> |
|データの種類 :   <br/> |PT_LONG  <br/> |
|エリア:  <br/> |アクセス制御のプロパティ  <br/> |
   
## <a name="remarks"></a>注釈

このプロパティは、クライアントの読み取り専用です。 これは、次のいずれかの値である必要があります。
  
|**値**|**説明**|
|:-----|:-----|
|0x00000000  <br/> |読み取り専用  <br/> |
|0x00000001  <br/> |変更  <br/> |
   
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連するプロトコル仕様へのExchange Server提供します。
    
[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> メッセージ オブジェクトと添付ファイル オブジェクトを処理します。
    
### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型の定義を提供します。
    
Mapitags.h
  
> 関連付けられたプロパティとして一覧表示されるプロパティの定義が含まれる。
    
## <a name="see-also"></a>関連項目



[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名を MAPI 名にマッピングする](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名を標準プロパティ名にマッピングする](mapping-mapi-names-to-canonical-property-names.md)

