---
title: 受信者の削除
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: f7495030-e3b8-4c7c-9e19-284ba820e846
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 39ad9792fce6c282725f40073bf103b0afb4aee6
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59584627"
---
# <a name="deleting-a-recipient"></a>受信者の削除

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
 **変更可能なコンテナーから 1 つ以上のアドレス帳エントリを削除するには**
  
- [IABContainer::D eleteEntries](iabcontainer-deleteentries.md)メソッドを呼び出し、削除するアドレス帳エントリを表すエントリ識別子の配列を渡します。 **DeleteEntries は** 、1 つ以上のMAPI_W_PARTIAL_COMPLETION削除できなかったという警告を返すメッセージを返す場合があります。 **HR_FAILED** マクロを使用してこの戻り値をテストし、問題の詳細が必要な場合は、コンテナーの [IMAPIProp::GetLastError](imapiprop-getlasterror.md)メソッドを呼び出します。 
    
削除されたエントリの [ADRENTRY](adrentry.md) 構造へのポインターをキャッシュに保持すると、そのエントリ識別子を使用してプロパティを取得できます。 これは、エントリが削除のマークのみ付いているためです。 MAPI は、デザインによってこれらのマークされたエントリへのアクセスレベルを維持します。 
  

