---
title: 受信者の削除
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f7495030-e3b8-4c7c-9e19-284ba820e846
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 9a3006b43eb9f210603ff3a3d890118e7fd61d7a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799891"
---
# <a name="deleting-a-recipient"></a>受信者の削除

  
  
**適用対象**: Outlook 
  
 **変更可能なコンテナーから 1 つまたは複数のアドレス帳のエントリを削除するのには**
  
- 削除するアドレス帳のエントリを表すエントリの識別子の配列を渡して、 [IABContainer::DeleteEntries](iabcontainer-deleteentries.md)メソッドを呼び出します。 **DeleteEntries**は、警告、MAPI_W_PARTIAL_COMPLETION、1 つまたは複数のエントリを削除できなかったことを示すためを返すことができます。 **HR_FAILED**マクロに戻り値をテストし、問題の詳細については、必要な場合は、コンテナーの[IMAPIProp::GetLastError](imapiprop-getlasterror.md)メソッドを呼び出します。 
    
キャッシュに削除されたエントリの[ADRENTRY](adrentry.md)構造体へのポインターを保持する場合、そのエントリの識別子を使用してプロパティを取得することができます。 エントリが削除用にマークするためです。 MAPI では、仕様ではこれらのマークを付けたエントリへのアクセスのレベルを維持します。 
  

