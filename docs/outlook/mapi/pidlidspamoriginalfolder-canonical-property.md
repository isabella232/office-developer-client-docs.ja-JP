---
title: PidLidSpamOriginalFolder 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidLidSpamOriginalFolder
api_type:
- COM
ms.assetid: 45846fe3-7ab3-4019-98bb-fe615889c31c
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 3410291b1fa449f00f240cca4bf53bb61624d835
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59630177"
---
# <a name="pidlidspamoriginalfolder-canonical-property"></a>PidLidSpamOriginalFolder 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
メッセージが迷惑メール フォルダーにフィルター処理される前に、メッセージが入っていたフォルダーを示します。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |dispidSpamOriginalFolder  <br/> |
|プロパティ セット:  <br/> |PSETID_Common  <br/> |
|長い ID (LID):  <br/> |0x0000859C  <br/> |
|データの種類 :   <br/> |PT_BINARY  <br/> |
|エリア:  <br/> |スパム  <br/> |
   
## <a name="remarks"></a>注釈

このプロパティの値は、メッセージが移動される前に含まれるフォルダーの **EntryID** です。 このプロパティは、メッセージがスパムとしてマークされている場合に設定する必要があります。 
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> プロパティ セットの定義と、関連するプロトコル仕様へのExchange Serverを提供します。
    
[[MS-OXCSPAM]](https://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)
  
> 許可/ブロック リストの処理と迷惑メール メッセージの決定を有効にできます。
    
### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型の定義を提供します。
    
## <a name="see-also"></a>関連項目



[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名を MAPI 名にマッピングする](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名を標準プロパティ名にマッピングする](mapping-mapi-names-to-canonical-property-names.md)

