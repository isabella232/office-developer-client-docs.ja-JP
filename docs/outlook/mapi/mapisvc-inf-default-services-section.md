---
title: MapiSvc.inf [既定のサービス] セクション
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: dec42f8d-0f5c-4665-b53a-11cbc58b8b76
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: a7906a9a5e953332dba5c4776c63bb433a937a5d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435321"
---
# <a name="mapisvcinf-default-services-section"></a>MapiSvc.inf [既定のサービス] セクション

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
[ **既定のサービス] セクション** には、既定のメッセージ サービスとして選択されているすべてのメッセージ サービスが一覧表示されます。 これらの既定のメッセージ サービスは、[サービス] セクションに記載されているメッセージ サービス **のサブセット** です。 プロファイル構成プログラムが既定のプロファイルを作成すると、このセクションのメッセージ サービスが自動的に含まれます。 
  
次に示すように、エントリは [ **サービス]** セクションのエントリと同じ形式を使用します。 
  
 **[既定のサービス]**
  
 _message-service セクション名_  =  _メッセージ サービス名_
  
次のエントリは、前の図に示す mapisvc.inf の [既定のサービス **]** セクションに含まれます。 
  
```cpp
[Default Services]
AB=Default Address Book
MsgService=My Own Service

```


