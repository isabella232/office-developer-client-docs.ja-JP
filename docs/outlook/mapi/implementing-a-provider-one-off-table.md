---
title: プロバイダーの一時テーブルを実装します。
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 8b0dcbfe-6bed-4fb8-a906-009f1d009055
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 99146f93dcf634be6766f5c6fcc0d1c610b84d4d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800923"
---
# <a name="implementing-a-provider-one-off-table"></a>プロバイダーの一時テーブルを実装します。

  
  
**適用されます**: Outlook 
  
MAPI は、クライアント アプリケーションのユーザーは、送信メッセージに受信者を追加するときに、プロバイダーの[IABLogon::GetOneOffTable](iablogon-getoneofftable.md)メソッドを呼び出します。 通常、要求されたアドレスの種類は、メッセージング システムに固有です。 プロバイダーは、受信者の作成をサポートする場合、サポートされている受信者のアドレスの種類ごとにテンプレートを公開する一時テーブルが必要です。 プロバイダーが受信者の作成をサポートしていない場合は、 **GetOneOffTable**の呼び出しから MAPI_E_NO_SUPPORT を返します。 
  
MAPI は通常、プロバイダーの一時テーブルを開いたまま、セッションの有効期間をクライアントが呼び出すサブシステムの場合にのみそれを解放するか、ブックの[IMAPIStatus::ValidateState](imapistatus-validatestate.md)メソッドに対応します。 MAPI をするよう、ユーザーにこれらの変更を反映できる場合は、テンプレートを追加または削除、このテーブルで通知を登録します。 
  
 **IABLogon::GetOneOffTable を実装するには**
  
1. _UlFlags_、flags パラメーターの値を確認してください。 MAPI_UNICODE フラグが設定されて、プロバイダーが Unicode をサポートしていない場合は、失敗し、MAPI_E_BAD_CHARWIDTH を返します。 
    
2. プロバイダーの一時テーブルが既に作成されているを確認します。 一時テーブルは静的であるため、プロバイダーが複数回作成プロセスを経由します。 テーブルが既に存在する場合、それへのポインターを返します。 
    
3. 一時テーブルが存在しない場合は、1 つを作成するのには、 **CreateTable**を呼び出します。 
    
4. テーブル行の列の次のプロパティを設定します。
    
  - **PR_DISPLAY_NAME**([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) にテンプレートを作成できる受信者の種類の名前。 
    
  - **PR_ENTRYID**([PidTagEntryId](pidtagentryid-canonical-property.md)) に 1 回限りのテンプレートのエントリの識別子です。
    
  - **PR_DEPTH**([PidTagDepth](pidtagdepth-canonical-property.md)) の 1 回限りの一覧が表示階層レベルを示す。
    
  - **PR_SELECTABLE**([PidTagSelectable](pidtagselectable-canonical-property.md)) かどうか、行を表すテンプレートと FALSE それ以外の場合を示すために TRUE に設定します。
    
  - **PR_ADDRTYPE**([PidTagAddressType](pidtagaddresstype-canonical-property.md)) のテンプレートで作成されたアドレスの種類にします。
    
  - **PR_DISPLAY_TYPE**([PidTagDisplayType](pidtagdisplaytype-canonical-property.md)) DT_MAILUSER またはテンプレートの表示の種類を示す別の値にします。
    
  - **PR_INSTANCE_KEY**([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) に固有のバイナリ値です。 
    
5. テーブルを直接変更するのには[ITableData::HrModifyRow](itabledata-hrmodifyrow.md)を呼び出します。 
    
6. 呼び出し元に戻るには**IMAPITable**インターフェイスの実装を作成するのには、 [ITableData::HrGetView](itabledata-hrgetview.md)を呼び出します。 
    

