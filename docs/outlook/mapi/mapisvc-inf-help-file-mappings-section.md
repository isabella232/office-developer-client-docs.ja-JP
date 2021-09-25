---
title: MapiSvc.inf [ヘルプ ファイル マッピング] セクション
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 62aee641-b73f-4f53-9e8d-adf010c9ea1a
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 2192421ddcde6771fa0eb342fc07aa28a65ddc51
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59575443"
---
# <a name="mapisvcinf-help-file-mappings-section"></a>MapiSvc.inf [ヘルプ ファイル マッピング] セクション

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
[ **ヘルプ ファイル マッピング] セクション** には、各サービスが 1 つのメッセージ サービスをファイルにマップし、サービスによって生成されたエラーのヘルプを提供するエントリが含まれています。 このセクションのエントリでは、次の形式を使用します。 
  
 **[ヘルプ ファイル マッピング] メッセージ**_サービス名 ヘルプ_  =   _ファイル名_
  
メッセージ サービス名は、インストールされているメッセージ サービスの名前です。ヘルプ ファイル名は、エラー情報が存在するファイルの名前です。 次の例は、MAPI、MsgService サービス、MS サービスの 3 つのサービスのエントリを含む一般的な [ヘルプ ファイル マッピング **]** セクションを示しています。 
  
```cpp
[Help File Mappings]
MAPI=MAPI.HLP
MsgService=MYHELP.HLP
MS=STORE.HLP

```


