---
title: 受信者の削除
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f7495030-e3b8-4c7c-9e19-284ba820e846
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: bd01c66d9fff7c94ffb1ce9f956f1951bc482020
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421047"
---
# <a name="deleting-a-recipient"></a>受信者の削除

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
 **変更可能なコンテナーから1つまたは複数のアドレス帳のエントリを削除するには**
  
- [IABContainer::D eleteentries](iabcontainer-deleteentries.md)メソッドを呼び出して、削除するアドレス帳のエントリを表すエントリ識別子の配列を渡します。 **deleteentries**は、1つまたは複数のエントリを削除できなかったことを示すために、MAPI_W_PARTIAL_COMPLETION という警告を返すことができます。 **HR_FAILED**マクロを使用してこの戻り値をテストし、問題に関する詳細情報が必要な場合は、コンテナーの[imapiprop:: GetLastError](imapiprop-getlasterror.md)メソッドを呼び出します。 
    
キャッシュ内の削除されたエントリの[adrentry](adrentry.md)構造体へのポインターを保持する場合でも、そのエントリ識別子を使用してプロパティを取得できます。 これは、エントリが削除対象としてマークされているためです。 MAPI では、これらのマークされたエントリに対して、設計によるレベルのアクセスが維持されます。 
  

