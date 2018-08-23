---
title: ステータス オブジェクトの実装
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 48fd3e28-c2d2-474d-9487-5e2f08ca7319
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: e019ad8d0063514cd41017b459cc701c45c22a2e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22569597"
---
# <a name="status-object-implementation"></a>ステータス オブジェクトの実装

**適用されます**: Outlook 2013 |Outlook 2016 
  
すべてのサービス プロバイダーは、状態オブジェクトを実装し、セッション ・ ステータス ・ テーブルからのプロパティを提供する必要があります。 制御するリソースの数によっては、状態テーブルでは、1 つまたは複数の行を含めることができます。 たとえば、トランスポート プロバイダーは、状態テーブルには、各メッセージ キューの管理行を作成する必要があります。 を変更した場合は、適切な状態のテーブルの行を更新しなければなりません。 状態オブジェクトを実装すると、状態テーブルに含まれている情報およびテーブルに含まれていないその他の情報へのアクセスを提供できます。
  
### <a name="to-implement-a-status-object"></a>状態オブジェクトを実装するには

1. ログオン オブジェクトの**OpenStatusEntry**メソッドを実装します。 クライアントは、状態オブジェクトを開く場合、それらは[IMAPISession::OpenEntry](imapisession-openentry.md)を呼び出します。 MAPI は、その状態オブジェクトを開き、その**IMAPIStatus**実装へのポインターをクライアントに返すには、プロバイダーの原因と、プロバイダーの**OpenStatusEntry**メソッドを呼び出すことによって、開く操作の要求を満たします。 実装では、 **OpenStatusEntry** 、次の手順を行います。 
    
   1. ログオン オブジェクトが状態オブジェクトをまだ作成していない場合は、次のタスクを実行します。
    
      1. プロバイダーのプロファイル セクションにアクセスするためのサポート オブジェクトの[IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md)メソッドを呼び出します。 
          
      2. 新しい状態オブジェクトを作成します。
          
      3. プロファイル セクションへの参照をプロバイダーの状態のオブジェクトに格納し、メソッドを呼び出してプロファイル セクションの[IUnknown::AddRef](http://msdn.microsoft.com/library/b4316efd-73d4-4995-b898-8025a316ba63%28Office.15%29.aspx)を参照カウントをインクリメントします。 
          
      4. ログオン オブジェクトへの参照をプロバイダーの状態のオブジェクトに格納し、参照カウントをインクリメントするのには、ログオン オブジェクトの**IUnknown::AddRef**メソッドを呼び出します。 
          
      5. プロバイダーのログオン オブジェクトでは、状態オブジェクトへの参照を格納します。
    
   2. ログオン オブジェクトでは、その参照カウントをインクリメントするのには、状態オブジェクトの**IUnknown::AddRef**メソッドを呼び出します。 
    
   3. MAPI_STATUS するには、状態オブジェクトの**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md)) のプロパティを設定します。
    
   4. 状態のオブジェクト] をポイントして、 _lppMAPIStatus_の出力パラメーターを設定します。 
    
   5. _UlFlags_の入力パラメーターをチェックします。 MAPI_MODIFY に設定されている場合は、プロバイダーがその状態のオブジェクトへの読み取り/書き込みアクセスをサポートして、書き込み可能なオブジェクトを返します。 ただし、プロバイダーがその状態のオブジェクトへの読み取り/書き込みアクセスをサポートしていない場合は失敗しません。 読み取り専用である状態のオブジェクトを返します。 読み取り/書き込みステータスのオブジェクトを受信することがあるクライアントは、変更する前に、読み取り/書き込み権限が付与されているを確認してください。 
    
2. すべて必要なステータスのオブジェクトとステータス ・ テーブルのプロパティを設定します。 状態のテーブルの行に含まれるプロパティは、状態のオブジェクトを計算する MAPI プロパティを通じて使用可能なはずです。 必要なプロパティは次のとおりです。
    
   - **PR_DISPLAY_NAME**([PidTagDisplayName](pidtagdisplayname-canonical-property.md))
    
   - **PR_PROVIDER_DLL_NAME**([PidTagProviderDllName](pidtagproviderdllname-canonical-property.md))
    
   - **PR_PROVIDER_DISPLAY**([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md))
    
   - **PR_RESOURCE_TYPE**([PidTagResourceType](pidtagresourcetype-canonical-property.md))
    
   - **PR_RESOURCE_METHODS**([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md))
    
   - **PR_RESOURCE_FLAGS**([PidTagResourceFlags](pidtagresourceflags-canonical-property.md))
    
   - **PR_STATUS_CODE**([PidTagStatusCode](pidtagstatuscode-canonical-property.md))
    
3. 実装、 [IMAPIStatus: IMAPIProp](imapistatusimapiprop.md)は、プロバイダーの適切なメソッドです。 、プロバイダーによっては、 **IMAPIStatus**内のすべての 4 つのメソッドを実装する必要はありません。 すべてのプロバイダーのメソッドの読み取り専用バージョンを実装する必要があります、 [IMAPIProp: IUnknown](imapipropiunknown.md)インタ フェースと[IMAPIStatus::ValidateState](imapistatus-validatestate.md)メソッドです。 

   トランスポート プロバイダーは、 [IMAPIStatus::FlushQueues](imapistatus-flushqueues.md)も実装する必要があり、すべてのプロバイダーは、 [IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md)をサポートする必要があります。 [ただし、IMAPIStatus::ChangePassword](imapistatus-changepassword.md)は省略可能、サポートします。 パスワードを必要とし、それらをプログラムで変更できるようにするサービス ・ プロバイダーだけでは、このメソッドを実装する必要があります。 サポートしているすべてのメソッドの**PR_RESOURCE_METHODS**プロパティに対応するビットを設定します。 たとえば、 **ValidateState**と**SettingsDialog**をのみサポートする、次の**PR_RESOURCE_METHODS**を設定します。 
    
   `STATUS_VALIDATE_STATE | STATUS_SETTINGS_DIALOG`
    
   クライアントでは、状態オブジェクトを呼び出す前に**PR_RESOURCE_METHODS**の値を確認する必要があります。 MAPI_E_NO_SUPPORT を返すことによって、サポートされていないメソッドのいずれかの呼び出しを処理します。 
    
4. ステータス テーブルに、行または列を追加するのにはログオン時に[IMAPISupport::ModifyStatusRow](imapisupport-modifystatusrow.md)を呼び出します。 行の列情報と_ulFlags_パラメーターに 0 を含むプロパティ値の配列を渡します。 セッションの後のある時点で、プロバイダーの状態の変更が必要になります列の情報を更新するのには場合、STATUSROW_UPDATE フラグを設定して**ModifyStatusRow**をもう一度呼び出します。 
    
ステータス オブジェクトの詳細については、 [MAPI オブジェクトのステータス](mapi-status-objects.md)を参照してください。
  
## <a name="see-also"></a>関連項目

- [MAPI サービス プロバイダー](mapi-service-providers.md)

