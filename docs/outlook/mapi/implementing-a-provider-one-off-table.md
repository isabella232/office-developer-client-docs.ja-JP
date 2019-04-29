---
title: プロバイダーの1回限りのテーブルの実装
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 8b0dcbfe-6bed-4fb8-a906-009f1d009055
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 023686702b76b5b29acf4304fcfdb3377e8cfcff
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436294"
---
# <a name="implementing-a-provider-one-off-table"></a>プロバイダーの1回限りのテーブルの実装

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
クライアントアプリケーションのユーザーが送信メッセージに受信者を追加すると、MAPI はプロバイダーの[IABLogon:: getoneofftable](iablogon-getoneofftable.md)メソッドを呼び出します。 通常、要求されるアドレスの種類は、メッセージングシステムに固有のものです。 プロバイダーが受信者の作成をサポートしている場合、サポートされている受信者アドレスの種類ごとにテンプレートを公開する、1回限りのテーブルを提供する必要があります。 プロバイダーが受信者の作成をサポートしていない場合は、 **getoneofftable**呼び出しから MAPI_E_NO_SUPPORT を返します。 
  
通常、MAPI はプロバイダーの1回限りのテーブルを開いたままにします。セッションの有効期間は、クライアントがサブシステムまたはアドレス帳の[imapistatus:: validatestate](imapistatus-validatestate.md)メソッドを呼び出した場合に限られます。 この表の MAPI は、テンプレートが追加または削除された場合に、ユーザーに変更を反映することができるようにするために、この表の通知を登録します。 
  
 **IABLogon:: getoneofftable を実装するには**
  
1. flags パラメーターの_ulflags_の値を確認します。 MAPI_UNICODE フラグが設定されており、プロバイダーが UNICODE をサポートしていない場合は、fail および MAPI_E_BAD_CHARWIDTH を返します。 
    
2. プロバイダーの1回限りのテーブルが既に作成されているかどうかを確認します。 通常、1回限りのテーブルは静的であるため、プロバイダーは作成プロセスを複数回実行する必要はありません。 テーブルが既に存在する場合は、そのテーブルへのポインターを返します。 
    
3. 1回限りのテーブルがまだ存在しない場合は、 **CreateTable**を呼び出して、1つのテーブルを作成します。 
    
4. 表の行の列に対して次のプロパティを設定します。
    
  - **PR_DISPLAY_NAME**([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) を使用して、テンプレートが作成できる受信者の種類の名前を指定します。 
    
  - **PR_ENTRYID**([PidTagEntryId](pidtagentryid-canonical-property.md)) は、1回限りのテンプレートのエントリ識別子を示します。
    
  - **PR_DEPTH**([PidTagDepth](pidtagdepth-canonical-property.md)) は、1回限りのテーブル表示で階層レベルを示します。
    
  - **PR_SELECTABLE**([PidTagSelectable](pidtagselectable-canonical-property.md)) を TRUE にして、行がテンプレートを表しているかどうかを示します。それ以外の場合は FALSE を指定します。
    
  - **PR_ADDRTYPE**([PidTagAddressType](pidtagaddresstype-canonical-property.md)) は、テンプレートによって作成されたアドレスの種類を示します。
    
  - **PR_DISPLAY_TYPE**([PidTagDisplayType](pidtagdisplaytype-canonical-property.md)) から DT_MAILUSER またはテンプレートの表示の種類を示す別の値を指定します。
    
  - **PR_INSTANCE_KEY**([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) を一意のバイナリ値にします。 
    
5. テーブルを直接変更するには、 [itabledata:: hrmodifyrow](itabledata-hrmodifyrow.md)を呼び出します。 
    
6. 呼び出し元に返す**IMAPITable**インターフェイス実装を作成するには、 [itabledata:: hrgetview](itabledata-hrgetview.md)を呼び出します。 
    

