---
title: アドレス帳エントリの比較
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: e375367b-d107-4768-95de-00b8b9dc3511
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 1a4a06a76ec9bb7d46de9d13d42cfca00c2c353b
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59571998"
---
# <a name="comparing-address-book-entries"></a>アドレス帳エントリの比較

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
プロバイダーの [IABLogon::CompareEntryIDs](iablogon-compareentryids.md) 実装は、プロバイダーの 2 つのオブジェクトのエントリ識別子を比較します。 MAPI は、2 つのエントリ識別子にプロバイダーの登録済み MAPIUID が含まれていると判断した後、このメソッド [を呼び出します](mapiuid.md)。 そのため **、CompareEntryIDs** メソッドは  _、lpEntryID1_ および  _lpEntryID2_ パラメーターに渡されたエントリ識別子がプロバイダーに属している必要はありません。 
  
**IABLogon::CompareEntryIDs** の呼び出しは **、2** つのオブジェクトごとに PR_RECORD_KEY ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)) プロパティを取得し、それらを直接比較するのと同じです。
  
 **CompareEntryIds を実装する方法**
  
1. プロバイダーが情報を格納している場合は、渡されたエントリ識別子の種類を確認します。 たとえば、1 つのエントリ識別子がメッセージング ユーザーに属し、もう一方が配布リストに属している可能性があります。 型が一致しない場合は  _、lpulResult_ パラメーターの内容を FALSE に設定して返します。 
    
2. 2 つのエントリ識別子のサイズを比較します。 同じではない場合は  _、lpulResult_ パラメーターの内容を FALSE に設定して戻します。 
    
3. エントリ識別子のサイズが、その種類に対して正しいサイズである必要があることを確認します。 指定しない場合は  _、lpulResult_ パラメーターの内容を FALSE に設定し、エラー値を false にMAPI_E_UNKNOWN_ENTRYID。 
    
4. エントリ識別子が同じか確認します。 等しく比較する場合は  _、lpulResult_ パラメーターの内容を TRUE に設定して返します。 それ以外の場合は、返す前に FALSE に設定します。 
    
5. プロバイダーが短期エントリ識別子と長期識別子を比較している場合は、同じように比較する必要があります。
    

