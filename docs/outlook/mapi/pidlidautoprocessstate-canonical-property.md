---
title: PidLidAutoProcessState 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidLidAutoProcessState
api_type:
- COM
ms.assetid: 9e724af6-5b56-4eb3-a94c-1015ebce197c
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 407a3ef2c40f190714ce3577a39242d0f7664d7e
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59567040"
---
# <a name="pidlidautoprocessstate-canonical-property"></a>PidLidAutoProcessState 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
電子メール メッセージの自動処理で使用されるオプションを指定します。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |dispidSniffState  <br/> |
|プロパティ セット:  <br/> |PSETID_Common  <br/> |
|長い ID (LID):  <br/> |0x0000851A  <br/> |
|データの種類 :   <br/> |PT_LONG  <br/> |
|エリア:  <br/> |一般的なメッセージング  <br/> |
   
## <a name="remarks"></a>注釈

プロパティが存在しない場合、既定値の "0x00000000" が使用されます。 このプロパティを設定する場合は、次の表のいずれかの値に設定する必要があります。
  
|**値**|**説明**|
|:-----|:-----|
|0x00000000  <br/> |メッセージを自動的に処理しない。  <br/> |
|0x00000001  <br/> |メッセージを自動的に処理するか、メッセージを開いたときに処理します。  <br/> |
|0x00000002  <br/> |メッセージを処理できるのは、メッセージを開いた場合のみです。  <br/> |
   
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> プロパティ セットの定義と、関連するプロトコル仕様へのExchange Serverを提供します。
    
[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> 電子メール メッセージ オブジェクトで許容されるプロパティと操作を指定します。
    
### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型の定義を提供します。
    
## <a name="see-also"></a>関連項目



[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名を MAPI 名にマッピングする](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名を標準プロパティ名にマッピングする](mapping-mapi-names-to-canonical-property-names.md)

