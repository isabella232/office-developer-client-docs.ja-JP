---
title: PidLidSpamOriginalFolder 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidSpamOriginalFolder
api_type:
- COM
ms.assetid: 45846fe3-7ab3-4019-98bb-fe615889c31c
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 561008782e7c1ffb8bc71cf4e3bc17befe69bbca
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331557"
---
# <a name="pidlidspamoriginalfolder-canonical-property"></a>PidLidSpamOriginalFolder 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
メッセージが迷惑メールフォルダーにフィルター処理されるまでのフォルダーを示します。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |dispidSpamOriginalFolder  <br/> |
|プロパティセット:  <br/> |PSETID_Common  <br/> |
|ロング ID (LID):  <br/> |0x0000859C  <br/> |
|データの種類 :   <br/> |PT_BINARY  <br/> |
|エリア:  <br/> |スパム  <br/> |
   
## <a name="remarks"></a>解説

このプロパティの値は、移動前にメッセージが含まれていたフォルダーの**EntryID**です。 このプロパティは、メッセージがスパムとしてマークされている場合に設定する必要があります。 
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> プロパティセットの定義と、関連する Exchange Server プロトコルの仕様への参照を提供します。
    
[[OXCSPAM]](https://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)
  
> 許可/ブロックリストの処理と、迷惑メールメッセージの決定を有効にします。
    
### <a name="header-files"></a>ヘッダーファイル

mapidefs.h
  
> データ型定義を提供します。
    
## <a name="see-also"></a>関連項目



[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名から MAPI 名へのマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名から標準プロパティ名へのマッピング](mapping-mapi-names-to-canonical-property-names.md)

