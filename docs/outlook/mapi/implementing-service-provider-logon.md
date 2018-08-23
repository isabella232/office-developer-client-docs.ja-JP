---
title: サービス プロバイダー ログオンの実装
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 3d3c309f-fe60-43a9-beda-16b09ec769db
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 1baa987961eecc6ee08b3ceb039062c8f1090ff7
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22589554"
---
# <a name="implementing-service-provider-logon"></a>サービス プロバイダー ログオンの実装

**適用されます**: Outlook 2013 |Outlook 2016 
  
MAPI は、エントリ ポイント関数から返すするポインターを使用してログオン プロセスを開始するのには、プロバイダーのオブジェクトでメソッドを呼び出します。 方法は異なります、サービス ・ プロバイダーの種類によって次のように。
  
- アドレス帳プロバイダーの[IABProvider::Logon](iabprovider-logon.md) 
    
- メッセージ ストア プロバイダーの[IMSProvider::Logon](imsprovider-logon.md) 
    
- トランスポート プロバイダーの[IXPProvider::TransportLogon](ixpprovider-transportlogon.md) 
    
ログオン方法を実装するには、次のタスクを実行します。
  
1. [IUnknown::AddRef](http://msdn.microsoft.com/en-us/library/ms691379%28v=VS.85%29.aspx)メソッドを呼び出して、入力パラメーターとして渡されるサポート オブジェクトの参照カウントをインクリメントします。 
    
2. [プロファイル] セクションにアクセスするためのサポート オブジェクトの[IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md)メソッドを呼び出します。 
    
3. 次のプロパティを設定するのには、プロファイルのセクションの[IMAPIProp::SetProps](imapiprop-setprops.md)メソッドを呼び出します。 
    
  - **PR_DISPLAY_NAME**([PidTagDisplayName](pidtagdisplayname-canonical-property.md))
    
  - **PR_ENTRYID**([PidTagEntryId](pidtagentryid-canonical-property.md))
    
  - **PR_PROVIDER_DISPLAY**([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md))
    
  - **PR_RECORD_KEY**([PidTagRecordKey](pidtagrecordkey-canonical-property.md))
    
  > [!NOTE]
  > プロファイル セクションの**PR_RESOURCE_FLAGS**または**PR_PROVIDER_DLL_NAME**のプロパティを設定しないでください。 ログオン時に、これらのプロパティは読み取り専用です。 
  
4. プロパティを構成する必要がありますがプロファイルに格納されるか、またはユーザーから利用できることを確認してください。 構成の確認の詳細については、[サービス プロバイダーの構成を確認する](verifying-service-provider-configuration.md)を参照してください。
    
5. プロバイダーがアドレス帳またはメッセージ ストア プロバイダーの場合は、一意の識別子、または[MAPIUID](mapiuid.md)、登録のサポート オブジェクトの[IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md)メソッドを呼び出します。 トランスポート プロバイダーは、MAPI は、 [IXPLogon::AddressTypes](ixplogon-addresstypes.md)メソッドを呼び出すと、 **MAPIUID**構造体を登録します。 の**MAPIUID**を登録の詳細については、[登録するサービス プロバイダー固有の識別子](registering-service-provider-unique-identifiers.md)を参照してください。
    
6. ログオン オブジェクトをインスタンス化し、次の値のいずれかを返します。
    
  - ログオンが成功を示すために S_OK です。
    
  - 構成のプロパティの 1 つ以上を示すために MAPI_E_UNCONFIGURED を使用できませんでした。
    
  - ユーザー キャンセルされたこと [構成] ダイアログ ボックスが使用できない設定のプロパティの原因を示すために MAPI_E_USER_CANCEL。
    
  - プロバイダーを構成できませんでしたが、MAPI に関係なく使用することを許可する必要があることを示すために MAPI_E_FAILONEPROVIDER。 ログオン方法には、プロバイダーがパスワードが必要ですし、ユーザー インターフェイスが無効であるため、ユーザーに確認ことはできませんなど、致命的でないエラーを報告するには、この値を返す必要があります。 
    
上記のタスクの一覧では、サービス プロバイダーのログオン方法の最低限の実装について説明します。 必要に応じて、追加の機能を含めることができます。 など、一部のプロバイダーは、そのログオン方法で状態テーブルを更新する[IMAPISupport::ModifyStatusRow](imapisupport-modifystatusrow.md)を呼び出します。 
  
> [!NOTE]
> ログオン時に最高のパフォーマンスを達成するために[IMAPISupport::PrepareSubmit](imapisupport-preparesubmit.md)または[IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md)のいずれかの呼び出しを避けるためです。 これらの呼び出しが完了し、ログオン メソッドに制御を返すことができます、前に MAPI スプーラーを起動する必要があります。 
  
## <a name="see-also"></a>関連項目

- [サービス プロバイダーの開始](starting-a-service-provider.md)

