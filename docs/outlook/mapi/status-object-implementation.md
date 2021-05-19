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
  
すべてのサービス プロバイダーは、状態オブジェクトを実装し、そこからセッション状態テーブルにプロパティを提供する必要があります。 制御するリソースの数に応じて、状態テーブルに 1 つ以上の行を含めできます。 たとえば、トランスポート プロバイダーは、管理する各メッセージ キューの状態テーブルに行を作成する必要があります。 変更が発生した場合は、適切な状態テーブル行を更新する必要があります。 Status オブジェクトは、状態テーブルに含まれる情報と、テーブルに含まれていない追加情報へのアクセスを提供するために実装されます。
  
### <a name="to-implement-a-status-object"></a>状態オブジェクトを実装するには

1. ログオン オブジェクト **の OpenStatusEntry** メソッドを実装します。 クライアントが status オブジェクトを開く場合は [、IMAPISession::OpenEntry を呼び出します](imapisession-openentry.md)。 MAPI は、プロバイダーの **OpenStatusEntry** メソッドを呼び出して開いている要求を満たし、プロバイダーが状態オブジェクトを開き **、IMAPIStatus** 実装へのポインターをクライアントに返します。 **OpenStatusEntry 実装で**、次の手順を実行します。 
    
   1. ログオン オブジェクトがまだ状態オブジェクトを作成していない場合は、次のタスクを実行します。
    
      1. サポート オブジェクトの [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md) メソッドを呼び出して、プロバイダーのプロファイル セクションにアクセスします。 
          
      2. 新しい状態オブジェクトを作成します。
          
      3. プロバイダーの状態オブジェクトにプロファイル セクションへの参照を格納し、プロファイル セクションの [IUnknown::AddRef](https://msdn.microsoft.com/library/b4316efd-73d4-4995-b898-8025a316ba63%28Office.15%29.aspx) メソッドを呼び出して、参照カウントを増やします。 
          
      4. プロバイダーの状態オブジェクトにログオン オブジェクトへの参照を格納し、ログオン オブジェクトの **IUnknown::AddRef** メソッドを呼び出して参照カウントを増やします。 
          
      5. プロバイダーのログオン オブジェクトに status オブジェクトへの参照を格納します。
    
   2. status オブジェクトの **IUnknown::AddRef** メソッドを呼び出して、ログオン オブジェクトの参照カウントを増やします。 
    
   3. status オブジェクトのプロパティ ([PidTagObjectType](pidtagobjecttype-canonical-property.md) **)** プロパティを PR_OBJECT_TYPE に設定MAPI_STATUS。
    
   4. _lppMAPIStatus 出力_ パラメーターを status オブジェクトをポイントして返す値を設定します。 
    
   5. _ulFlags 入力パラメーターを_ 確認します。 このオブジェクトが MAPI_MODIFYに設定され、プロバイダーが status オブジェクトへの読み取り/書き込みアクセスをサポートしている場合は、書き込み可能なオブジェクトを返します。 ただし、プロバイダーが status オブジェクトへの読み取り/書き込みアクセスをサポートしていない場合は、失敗しない。 読み取り専用の状態オブジェクトを返します。 読み取り/書き込み状態オブジェクトを受け取る必要があるクライアントは、変更を行う前に、読み取り/書き込みアクセス許可が付与されたことを確認する必要があります。 
    
2. 必要なすべての状態オブジェクトと状態テーブルのプロパティを設定します。 状態テーブルの行に含めるプロパティは、MAPI によって計算されるプロパティを除き、status オブジェクトで使用できる必要があります。 必要なプロパティは次のとおりです。
    
   - **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))
    
   - **PR_PROVIDER_DLL_NAME** ([PidTagProviderDllName](pidtagproviderdllname-canonical-property.md))
    
   - **PR_PROVIDER_DISPLAY** ([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md))
    
   - **PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md))
    
   - **PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md))
    
   - **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md))
    
   - **PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md))
    
3. プロバイダーに [適した IMAPIStatus : IMAPIProp](imapistatusimapiprop.md) メソッドを実装します。 プロバイダーによっては、IMAPIStatus で 4 つのメソッドのすべてが実装 **されている必要はなさそう**。 すべてのプロバイダーは [、IMAPIProp : IUnknown](imapipropiunknown.md) インターフェイスと [IMAPIStatus::ValidateState](imapistatus-validatestate.md) メソッドのメソッドの読み取り専用バージョンを実装する必要があります。 

   トランスポート プロバイダーは [IMAPIStatus::FlushQueues](imapistatus-flushqueues.md)も実装する必要があります。すべてのプロバイダーは [IMAPIStatus::SettingsDialog をサポートする必要があります](imapistatus-settingsdialog.md)。 ただし [、IMAPIStatus::ChangePassword のサポートは](imapistatus-changepassword.md) オプションです。 パスワードが必要で、ユーザーがパスワードを変更できるサービス プロバイダーだけが、このメソッドを実装する必要があります。 サポートするメソッドごとに、対応するビットを **PR_RESOURCE_METHODSします。** たとえば **、ValidateState** と **SettingsDialog** のみをサポートしている場合は **、次PR_RESOURCE_METHODS** 設定します。 
    
   `STATUS_VALIDATE_STATE | STATUS_SETTINGS_DIALOG`
    
   クライアントは、status オブジェクトを呼び **出す前PR_RESOURCE_METHODS** の値を確認する必要があります。 サポートされていないメソッドの呼び出しを処理するには、サポートされていないメソッドを返MAPI_E_NO_SUPPORT。 
    
4. ログオン [中に IMAPISupport::ModifyStatusRow](imapisupport-modifystatusrow.md) を呼び出して、行または行を状態テーブルに追加します。 行の列情報と  _ulFlags_ パラメーターの 0 を含むプロパティ値配列を渡します。 セッションの後でプロバイダーの状態が変更され、列情報を更新する必要がある場合は、STATUSROW_UPDATE フラグを設定して **ModifyStatusRow** を再度呼び出します。 
    
状態オブジェクトの詳細については、「MAPI Status [Objects」を参照してください](mapi-status-objects.md)。
  
## <a name="see-also"></a>関連項目

- [MAPI サービス プロバイダー](mapi-service-providers.md)

