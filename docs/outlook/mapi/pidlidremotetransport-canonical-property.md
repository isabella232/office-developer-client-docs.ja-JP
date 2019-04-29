---
title: PidLidRemoteTransport 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidRemoteTransport
api_type:
- COM
ms.assetid: b3b30d6a-05cd-4dd1-a162-20768f12e680
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: ddedc2ca0785be2fe4850ec3cfdf979d1e5f2798
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439444"
---
# <a name="pidlidremotetransport-canonical-property"></a>PidLidRemoteTransport 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
ヘッダーアイテムが関連付けられているアカウントを識別します。主に、サーバー機能に POP を適用するために使用します。 
  
|||
|:-----|:-----|
|関連付けられたプロパティ  <br/> |dispidremotexp  <br/> |
|プロパティセット:  <br/> |PSETID_Remote  <br/> |
|ロング ID (LID):  <br/> |0x00008f03  <br/> |
|データの種類 :   <br/> |PT_STRING8  <br/> |
|エリア:  <br/> |リモートメッセージ  <br/> |
   
## <a name="remarks"></a>注釈

このプロパティは、メッセージクラスが IPM であるメッセージにのみ関連しています。リモート. Microsoft Outlook では、フォルダー関連情報 (fai) メッセージ内の特定のストアにダウンロードされるさまざまなアカウントのマッピングを保持しますが、この情報をレジストリに保持することもできます。
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[OXPROPS]] 
  
> プロパティセットの定義と、関連する Exchange Server プロトコルの仕様への参照を提供します。
    
### <a name="header-files"></a>ヘッダーファイル

mapidefs.h
  
> データ型定義を提供します。
    
## <a name="see-also"></a>関連項目



[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名から MAPI 名へのマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名から標準プロパティ名へのマッピング](mapping-mapi-names-to-canonical-property-names.md)

