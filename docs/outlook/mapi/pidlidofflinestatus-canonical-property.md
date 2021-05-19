---
title: PidLidOfflineStatus 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidOfflineStatus
api_type:
- COM
ms.assetid: ee69f0c4-b552-4cfd-8a39-a822d414549e
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 537b45420390903d67722c074a1edcc04a0aede8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418835"
---
# <a name="pidlidofflinestatus-canonical-property"></a>PidLidOfflineStatus 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
[MS-LISTSWS] を実装するサーバー上のドキュメント ファイルの状態を決定します。
  
|||
|:-----|:-----|
|関連付けられたプロパティ  <br/> |dispidOfflineStatus  <br/> |
|プロパティ セット:  <br/> |PSETID_Common  <br/> |
|長い ID (LID):  <br/> |0x000085B9  <br/> |
|データの種類 :   <br/> |PT_LONG  <br/> |
|エリア:  <br/> |一般的なメッセージング  <br/> |
   
## <a name="remarks"></a>注釈

次の表に、このプロパティの値を示します。
  
|**値**|**説明**|
|:-----|:-----|
|0  <br/> |ドキュメントはチェックアウトされません。  <br/> |
|1  <br/> |ドキュメントは現在のユーザーにチェックアウトされます。  <br/> |
|2  <br/> |ドキュメントはチェックアウトされませんが、現在のユーザーは現在のコンピューターで編集用に保存されたファイルのコピーを持っています。  <br/> |
   
このプロパティはローカルで計算され、ユーザーがアイテムを別のアカウントにドラッグしない限り、いつでもサーバーに送信されません。 その場合、ユーザー定義のカスタム プロパティとして扱います。
  
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

