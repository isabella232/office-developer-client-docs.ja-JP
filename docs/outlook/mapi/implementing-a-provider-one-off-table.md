---
title: プロバイダー テーブルのOne-Offする
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 8b0dcbfe-6bed-4fb8-a906-009f1d009055
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 060f69c28484b8fe3a805af22ebe631c746425de
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59620787"
---
# <a name="implementing-a-provider-one-off-table"></a>プロバイダー テーブルのOne-Offする

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
MAPI は、クライアント アプリケーションのユーザーが受信者を送信メッセージに追加するときに、プロバイダーの [IABLogon::GetOneOffTable](iablogon-getoneofftable.md) メソッドを呼び出します。 通常、要求されるアドレスの種類はメッセージング システムに固有です。 プロバイダーが受信者の作成をサポートしている場合は、サポートされている受信者アドレスのすべての種類のテンプレートを公開する 1 回のテーブルを指定する必要があります。 プロバイダーが受信者の作成をサポートしていない場合は **、GetOneOffTable** 呼び出MAPI_E_NO_SUPPORTを返します。 
  
MAPI は通常、セッションの有効期間中、プロバイダーの一時テーブルを開いた状態に保ち、クライアントがサブシステムまたはアドレス帳の [IMAPIStatus::ValidateState](imapistatus-validatestate.md) メソッドを呼び出す場合にのみ解放します。 MAPI は、テンプレートが追加または削除された場合、これらの変更をユーザーに反映できるよう、このテーブルの通知を登録します。 
  
 **IABLogon::GetOneOffTable を実装するには**
  
1. flags パラメーター  _ulFlags の値を確認します_。 このフラグMAPI_UNICODE設定され、プロバイダーが Unicode をサポートしていない場合は、エラーが発生し、MAPI_E_BAD_CHARWIDTH。 
    
2. プロバイダーの 1 回のテーブルが既に作成済みか確認します。 通常、1 回のテーブルは静的なので、プロバイダーは作成プロセスを 2 回以上実行する必要がなされません。 テーブルが既に存在する場合は、そのテーブルへのポインターを返します。 
    
3. 1 回のテーブルがまだ存在しない場合は **、CreateTable を呼び出して** 作成します。 
    
4. テーブル行の列に対して、次のプロパティを設定します。
    
  - **PR_DISPLAY_NAME** [(PidTagDisplayName)](pidtagdisplayname-canonical-property.md)をテンプレートで作成できる受信者の種類の名前を指定します。 
    
  - **PR_ENTRYID** [(PidTagEntryId)](pidtagentryid-canonical-property.md)を一時テンプレートのエントリ識別子に設定します。
    
  - **PR_DEPTH** ([PidTagDepth](pidtagdepth-canonical-property.md)) を使用して、1 回のテーブル表示で階層レベルを示します。
    
  - **PR_SELECTABLE** ([PidTagSelectable](pidtagselectable-canonical-property.md)) を TRUE に設定して、行がテンプレートを表すかどうかを示し、それ以外の場合は FALSE を指定します。
    
  - **PR_ADDRTYPE** [(PidTagAddressType)](pidtagaddresstype-canonical-property.md)をテンプレートによって作成されたアドレスの種類に設定します。
    
  - **PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md)) を使用して、DT_MAILUSERの表示の種類を示す別の値を指定します。
    
  - **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) を一意のバイナリ値に変換します。 
    
5. [ITableData::HrModifyRow を呼び出して](itabledata-hrmodifyrow.md)、テーブルを直接変更します。 
    
6. [ITableData::HrGetView](itabledata-hrgetview.md)を呼び出して、呼び出し元に戻る **IMAPITable** インターフェイス実装を作成します。 
    

