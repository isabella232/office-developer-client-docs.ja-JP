---
title: mapisvc.inf [Default Services] セクション
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: dec42f8d-0f5c-4665-b53a-11cbc58b8b76
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: a7906a9a5e953332dba5c4776c63bb433a937a5d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32270071"
---
# <a name="mapisvcinf-default-services-section"></a>mapisvc.inf [Default Services] セクション

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
**[default Services]** セクションには、既定のメッセージサービスとして選択されているすべてのメッセージサービスが一覧表示されます。 これらの既定のメッセージサービスは、 **[services]** セクションにリストされているメッセージサービスのサブセットです。 プロファイル構成プログラムが既定のプロファイルを作成すると、このセクションのメッセージサービスが自動的に追加されます。 
  
これらのエントリは、次に示すように **[Services]** セクションのエントリと同じ形式を使用します。 
  
 **[既定のサービス]**
  
 _メッセージ-サービスセクション名_ =  _メッセージサービス名_
  
前の図に示したように、mapisvc.inf の **[Default Services]** セクションには次のエントリが含まれています。 
  
```cpp
[Default Services]
AB=Default Address Book
MsgService=My Own Service

```


