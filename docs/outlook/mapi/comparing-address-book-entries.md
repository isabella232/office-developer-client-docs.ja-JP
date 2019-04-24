---
title: アドレス帳エントリの比較
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: e375367b-d107-4768-95de-00b8b9dc3511
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 6ccd7a55c195b45b1fa83db6180efeacd41b968d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335533"
---
# <a name="comparing-address-book-entries"></a>アドレス帳エントリの比較

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
プロバイダーの[IABLogon:: compareentryids](iablogon-compareentryids.md)実装は、プロバイダーのオブジェクトの2つのエントリ id を比較します。 MAPI は、2つのエントリ識別子にプロバイダーの登録済み[MAPIUID](mapiuid.md)が含まれていることを確認した後、このメソッドを呼び出します。 そのため、 **compareentryids**メソッドは、 _lpEntryID1_パラメーターと_lpEntryID2_パラメーターに渡されたエントリ識別子がプロバイダーに属していることを確認する必要はありません。 
  
**IABLogon:: compareentryids**は、2つのオブジェクトの**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)) プロパティを取得して、それらを直接比較することと同じです。
  
 **compareentryids を実装するには**
  
1. プロバイダーに情報が格納されている場合は、渡されたエントリ識別子の種類を確認します。 たとえば、一方のエントリ識別子はメッセージングユーザーに属している可能性がありますが、一方は配布リストに属している場合があります。 型が一致しない場合は、 _l出 result_パラメーターの内容を FALSE に設定して戻ります。 
    
2. 2つのエントリ識別子のサイズを比較します。 同じでない場合は、 _l出 result_パラメーターの内容を FALSE に設定して返します。 
    
3. 入力識別子のサイズが、種類に適したサイズであることを確認します。 含まれていない場合は、 _lMAPI_E_UNKNOWN_ENTRYID result_パラメーターの内容を FALSE に設定し、エラー値を返します。 
    
4. エントリ識別子が同じであるかどうかを確認します。 同等に比較する場合は、 _l出 result_パラメーターの内容を TRUE に設定して返します。 それ以外の場合は、値を FALSE に設定してから返します。 
    
5. プロバイダーが短期的なエントリ識別子と長期識別子を比較している場合は、同等に比較する必要があります。
    

