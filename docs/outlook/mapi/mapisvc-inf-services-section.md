---
title: MapiSvc.inf [Services] セクション
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 99f8e623-3138-4def-9778-5580326111a5
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 226465baa7b66e8d3453435b62c70445d66420a8
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59604741"
---
# <a name="mapisvcinf-services-section"></a>MapiSvc.inf [Services] セクション

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
[ **サービス] セクションには** 、コンピューターにインストールされているメッセージ サービスが一覧表示されます。 このセクションのエントリでは、次の形式を使用します。 
  
 **[サービス]**
  
 _message-service セクション名_  =  _メッセージ サービス名_
  
message-service セクション名は、mapisvc.inf の他の場所にあるサービスの対応するセクションにこのエントリをリンクするメッセージ サービスによって定義される文字列です。 メッセージ サービス名は、インストールされているサービスの名前です。 次のセクションでは、既定のアドレス帳、自分のサービス、およびメッセージ ストア サービスの 3 つのメッセージ サービスを示します。 これらのサービスは架空の、説明のみを目的とします。 各メッセージ サービスの実装者は、このセクションのメッセージ サービスの適切なエントリを置き換える必要があります。
  
```cpp
[Services]
AB=Default Address Book
MsgService=My Own Service
MS=Message Store Service

```

このセクションの各エントリには、メッセージ サービスの情報が格納される独自の対応するセクションがあります。 たとえば、既定のアドレス帳の対応するセクションは [AB] と呼ばれる。
  

