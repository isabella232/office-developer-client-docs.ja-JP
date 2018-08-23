---
title: アドレス帳エントリの比較
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: e375367b-d107-4768-95de-00b8b9dc3511
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 808d5f4bfca15cae4ca7aab6758d3b5361813bd4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799797"
---
# <a name="comparing-address-book-entries"></a>アドレス帳エントリの比較

  
  
**適用対象**: Outlook 
  
[IABLogon::CompareEntryIDs](iablogon-compareentryids.md)プロバイダーは、プロバイダーのオブジェクトの 2 つのエントリ id を比較します。 MAPI は、 [MAPIUID](mapiuid.md)を登録して、プロバイダーを 2 つのエントリの識別子が含まれていることを確認した後に、このメソッドを呼び出します。 したがって、 **CompareEntryIDs**メソッドでは、 _lpEntryID1_および_lpEntryID2_パラメーターに渡されたエントリ id をプロバイダーに属している必要があります調べません。 
  
**IABLogon::CompareEntryIDs**の呼び出しは、2 つのオブジェクトごとに、 **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)) のプロパティを取得して、直接比較することと等価です。
  
 **CompareEntryIds を実装するには**
  
1. プロバイダーがその情報を保存する場合は渡されたエントリ id の種類を確認してください。 たとえば、1 つのエントリ id が属しているメッセージング ユーザーに配布リストに所属している他の中に。 型が一致しない場合は、false を指定し、戻り値に_lpulResult_パラメーターの内容を設定します。 
    
2. 2 つのエントリ id のサイズを比較します。 同じである場合は、FALSE を返す_lpulResult_パラメーターの内容を設定します。 
    
3. エントリ id のサイズが型に対して適切なサイズであることを確認します。 いない場合は、false を指定する_lpulResult_パラメーターの内容を設定し、MAPI_E_UNKNOWN_ENTRYID のエラー値を返します。 
    
4. エントリ id が同じかどうかを確認してください。 同様に、比較する場合は、true を指定し、戻り値に_lpulResult_パラメーターの内容を設定します。 それ以外の場合、FALSE に設定を返す前にします。 
    
5. 場合は、プロバイダーは、長期的な識別子を使用して、短期的なエントリ id を比較することは、同じように比較する必要があります。
    

