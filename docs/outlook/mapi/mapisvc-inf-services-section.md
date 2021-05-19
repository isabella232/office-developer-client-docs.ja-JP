---
title: MapiSvc.inf [Services] セクション
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 99f8e623-3138-4def-9778-5580326111a5
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: e5bf5242ef673976ebda928d6ce4862e3e7dd072
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434782"
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
  

