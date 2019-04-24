---
title: 状態オブジェクトの実装
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 48fd3e28-c2d2-474d-9487-5e2f08ca7319
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: e97efb70716ffbd7fa98f980ce8520cfcb988532
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32336338"
---
# <a name="status-object-implementation"></a>状態オブジェクトの実装

**適用対象**: Outlook 2013 | Outlook 2016 
  
すべてのサービスプロバイダーは、status オブジェクトを実装して、そのオブジェクトからのプロパティをセッション状態テーブルに提供する必要があります。 管理するリソースの数に応じて、[状態] テーブルに1つ以上の行を含めることができます。 たとえば、トランスポートプロバイダーは、管理する各メッセージキューの状態テーブルに行を作成する必要があります。 変更が発生した場合は、適切な状態テーブル行を更新する必要があります。 status オブジェクトは、状態テーブルに含まれている情報と、テーブルに含まれていない追加情報の両方にアクセスできるように実装されています。
  
### <a name="to-implement-a-status-object"></a>status オブジェクトを実装するには

1. ログオンオブジェクトの**openstatusentry**メソッドを実装します。 クライアントは、状態オブジェクトを開こうとすると、 [imapisession:: openentry](imapisession-openentry.md)を呼び出します。 MAPI はプロバイダーの**openstatusentry**メソッドを呼び出して open 要求を処理します。これにより、プロバイダーはその状態オブジェクトを開き、 **imapistatus**実装へのポインターをクライアントに返します。 **openstatusentry**実装で、次の手順を実行します。 
    
   1. ログオンオブジェクトがステータスオブジェクトをまだ作成していない場合は、次のタスクを実行します。
    
      1. サポートオブジェクトの[imapisupport:: openprofilesection](imapisupport-openprofilesection.md)メソッドを呼び出して、プロバイダーのプロファイルセクションにアクセスします。 
          
      2. 新しい status オブジェクトを作成します。
          
      3. プロバイダーの状態オブジェクトのプロファイルセクションへの参照を格納し、プロファイルセクションの[IUnknown:: AddRef](https://msdn.microsoft.com/library/b4316efd-73d4-4995-b898-8025a316ba63%28Office.15%29.aspx)メソッドを呼び出して、参照カウントをインクリメントします。 
          
      4. プロバイダーの status オブジェクトにログオンオブジェクトへの参照を格納し、ログオンオブジェクトの**IUnknown:: AddRef**メソッドを呼び出して、参照カウントをインクリメントします。 
          
      5. プロバイダーのログオンオブジェクトに状態オブジェクトへの参照を格納します。
    
   2. 状態オブジェクトの**IUnknown:: AddRef**メソッドを呼び出して、ログオンオブジェクトの参照カウントをインクリメントします。 
    
   3. status オブジェクトの**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md)) プロパティを MAPI_STATUS に設定します。
    
   4. _lppMAPIStatus_ output パラメーターを status オブジェクトを指すように設定し、を返します。 
    
   5. _ulflags_入力パラメーターを確認します。 MAPI_MODIFY に設定されており、プロバイダーがその状態オブジェクトへの読み取り/書き込みアクセスをサポートしている場合は、書き込み可能なオブジェクトを返します。 ただし、プロバイダーが status オブジェクトへの読み取り/書き込みアクセスをサポートしていない場合は、失敗しません。 読み取り専用の status オブジェクトを取得します。 読み取り/書き込み状態のオブジェクトを受信すると予想されるクライアントは、変更を行う前に読み取り/書き込みアクセス許可が付与されていることを確認する必要があります。 
    
2. 必要なすべての status オブジェクトおよび status テーブルのプロパティを設定します。 状態テーブルの行に含めるプロパティは、MAPI によって計算されたプロパティを除き、状態オブジェクトで使用できます。 必要なプロパティは次のとおりです。
    
   - **PR_DISPLAY_NAME**([PidTagDisplayName](pidtagdisplayname-canonical-property.md))
    
   - **PR_PROVIDER_DLL_NAME**([PidTagProviderDllName](pidtagproviderdllname-canonical-property.md))
    
   - **PR_PROVIDER_DISPLAY**([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md))
    
   - **PR_RESOURCE_TYPE**([PidTagResourceType](pidtagresourcetype-canonical-property.md))
    
   - **PR_RESOURCE_METHODS**([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md))
    
   - **PR_RESOURCE_FLAGS**([PidTagResourceFlags](pidtagresourceflags-canonical-property.md))
    
   - **PR_STATUS_CODE**([PidTagStatusCode](pidtagstatuscode-canonical-property.md))
    
3. プロバイダーに適した[imapistatus: imapistatus](imapistatusimapiprop.md)メソッドを実装します。 プロバイダーによっては、 **imapistatus**にすべての4つのメソッドを実装する必要はありません。 すべてのプロバイダーは、 [imapiprop: IUnknown](imapipropiunknown.md)インターフェイスおよび[imapiprop:: validatestate](imapistatus-validatestate.md)メソッドの読み取り専用バージョンを実装する必要があります。 

   また、トランスポートプロバイダーは[imapistatus:: flushqueues](imapistatus-flushqueues.md)を実装する必要があります。また、すべてのプロバイダーは[imapistatus:: settingsdialog](imapistatus-settingsdialog.md)をサポートする必要があります。 ただし、 [imapistatus:: ChangePassword](imapistatus-changepassword.md)のサポートはオプションです。 パスワードを必要とし、ユーザーがプログラムによって変更できるようにするサービスプロバイダーのみが、このメソッドを実装する必要があります。 サポートしているすべてのメソッドについて、 **PR_RESOURCE_METHODS**プロパティに対応するビットを設定します。 たとえば、 **validatestate**と**settingsdialog**のみをサポートする場合は、 **PR_RESOURCE_METHODS**を次のように設定します。 
    
   `STATUS_VALIDATE_STATE | STATUS_SETTINGS_DIALOG`
    
   クライアントは、status オブジェクトの呼び出しを試行する前に、 **PR_RESOURCE_METHODS**の値を確認する必要があります。 MAPI_E_NO_SUPPORT を返すことで、サポートされていないメソッドの呼び出しを処理します。 
    
4. 状態テーブルに行または行を追加するには、ログオン時に[imapisupport:: modifystatusrow](imapisupport-modifystatusrow.md)を呼び出します。 行の列情報を含むプロパティ値の配列、および_ulflags_パラメーターに0を渡します。 セッションの後の方の時点で、プロバイダーの状態が変化し、列情報を更新する必要が生じた場合は、STATUSROW_UPDATE フラグセットを使用して、再度**modifystatusrow**を呼び出します。 
    
状態オブジェクトの詳細については、「 [MAPI status objects](mapi-status-objects.md)」を参照してください。
  
## <a name="see-also"></a>関連項目

- [MAPI サービスプロバイダー](mapi-service-providers.md)

