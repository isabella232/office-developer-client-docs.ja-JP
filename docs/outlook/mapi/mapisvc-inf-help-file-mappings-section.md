---
title: mapisvc.inf [Help File Mappings] セクション
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 62aee641-b73f-4f53-9e8d-adf010c9ea1a
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 4760c9965975bb5d950e51b707d28bee647ef99a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407558"
---
# <a name="mapisvcinf-help-file-mappings-section"></a>mapisvc.inf [Help File Mappings] セクション

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
**[Help File Mappings]** セクションには、サービスによって生成されたエラーについてのヘルプを提供する1つのメッセージサービスをファイルにマップするエントリが含まれています。 このセクションのエントリは、次の形式を使用します。 
  
 **[Help File Mappings]**_メッセージサービス名_ =  _ヘルプファイル名_
  
メッセージサービス名は、インストールされているメッセージサービスの名前です。ヘルプファイル名は、エラー情報が格納されているファイルの名前です。 次の例は、3つのサービス (MAPI、msgservice サービス、および MS service) のエントリを含む標準的な **[Help File Mappings]** セクションを示しています。 
  
```cpp
[Help File Mappings]
MAPI=MAPI.HLP
MsgService=MYHELP.HLP
MS=STORE.HLP

```


