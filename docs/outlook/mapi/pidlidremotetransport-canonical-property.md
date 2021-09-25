---
title: PidLidRemoteTransport 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidLidRemoteTransport
api_type:
- COM
ms.assetid: b3b30d6a-05cd-4dd1-a162-20768f12e680
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 22b497aea3510e7bd2f54b2fd32bbf7dd6f6a16c
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59591746"
---
# <a name="pidlidremotetransport-canonical-property"></a>PidLidRemoteTransport 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
主に POP Leave on Server 機能を実装するために、ヘッダー アイテムが関連付けられているアカウントを識別します。 
  
|||
|:-----|:-----|
|関連付けられたプロパティ  <br/> |dispidRemoteXP  <br/> |
|プロパティ セット:  <br/> |PSETID_Remote  <br/> |
|長い ID (LID):  <br/> |0x00008F03  <br/> |
|データの種類 :   <br/> |PT_STRING8  <br/> |
|エリア:  <br/> |リモート メッセージ  <br/> |
   
## <a name="remarks"></a>注釈

このプロパティは、IPM のメッセージ クラスを持つメッセージにのみ関連します。リモート。 Microsoft Outlookは、フォルダー関連情報 (FAI) メッセージ内の特定のストアにダウンロードしているさまざまなアカウントのマッピングを保持しますが、この情報をレジストリに保持することもできます。
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS-OXPROPS]] 
  
> プロパティ セットの定義と、関連するプロトコル仕様へのExchange Serverを提供します。
    
### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型の定義を提供します。
    
## <a name="see-also"></a>関連項目



[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名を MAPI 名にマッピングする](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名を標準プロパティ名にマッピングする](mapping-mapi-names-to-canonical-property-names.md)

