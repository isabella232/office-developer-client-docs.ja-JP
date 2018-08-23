---
title: MapiSvc.inf [Services] セクション
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 99f8e623-3138-4def-9778-5580326111a5
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 19031f6c02f3e8e925adfc8d2affa43fb6532fee
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801531"
---
# <a name="mapisvcinf-services-section"></a>MapiSvc.inf [Services] セクション

  
  
**適用対象**: Outlook 
  
**[サービス]** セクションには、コンピューターにインストールされているメッセージ サービスが一覧表示されます。 このセクションのエントリは、次の形式を使用します。 
  
 **[サービス]**
  
 _メッセージ サービス セクション名_ =  _メッセージ サービス名_
  
メッセージ サービスのセクション名は文字列定義メッセージ サービスでリンクしているこのエントリ mapisvc.inf の他の場所でサービスの対応するセクションです。 メッセージ サービス名は、インストールされているサービスの名前です。 次のセクションでは、3 つのメッセージ サービスを示しています: 既定のアドレス帳、自分独自のサービス、およびメッセージ ストアのサービスです。 これらのサービスは、例示目的でのみ、架空されています。 各メッセージ サービスの実装側は、ここで自分のメッセージ サービスの適切なエントリではなきます。
  
```cpp
[Services]
AB=Default Address Book
MsgService=My Own Service
MS=Message Store Service

```

このセクションでは、各エントリには、メッセージ サービスの情報を格納する、独自の対応するセクションがあります。 たとえば、既定のアドレス帳の対応するセクションは、[AB] と呼ばれます。
  

