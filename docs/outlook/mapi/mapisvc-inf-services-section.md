---
title: mapisvc.inf [Services] セクション
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
# <a name="mapisvcinf-services-section"></a>mapisvc.inf [Services] セクション

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
**[Services]** セクションには、コンピューターにインストールされているメッセージサービスが表示されます。 このセクションのエントリは、次の形式を使用します。 
  
 **サービス**
  
 _メッセージ-サービスセクション名_ =  _メッセージサービス名_
  
メッセージサービスセクション名は、このエントリを mapisvc.inf 内の他の場所にあるサービスの対応するセクションにリンクするメッセージサービスによって定義された文字列です。 メッセージサービス名は、インストールされているサービスの名前です。 次のセクションでは、既定のアドレス帳、独自のサービス、およびメッセージストアサービスという3つのメッセージサービスについて説明します。 これらのサービスは架空のものであり、説明のみを目的としています。 各メッセージサービスの実装者は、このセクションでメッセージサービスの適切なエントリを置き換えます。
  
```cpp
[Services]
AB=Default Address Book
MsgService=My Own Service
MS=Message Store Service

```

このセクションの各エントリには、メッセージサービスの情報が格納されている場所に対応するセクションがあります。 たとえば、既定のアドレス帳の対応するセクションは [AB] と呼ばれます。
  

