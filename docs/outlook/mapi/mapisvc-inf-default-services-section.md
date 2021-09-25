---
title: MapiSvc.inf [既定のサービス] セクション
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: dec42f8d-0f5c-4665-b53a-11cbc58b8b76
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: e99fec901bac6f72ac1ded4934896fd3869e89b6
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59595757"
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


