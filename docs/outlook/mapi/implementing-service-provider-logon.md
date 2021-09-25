---
title: サービス プロバイダー ログオンの実装
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 3d3c309f-fe60-43a9-beda-16b09ec769db
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 5651ab674071b832eb14d2ca217bd8cf0fa90196
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59575695"
---
# <a name="implementing-service-provider-logon"></a>サービス プロバイダー ログオンの実装

**適用対象**: Outlook 2013 | Outlook 2016 
  
MAPI は、プロバイダー オブジェクト内のメソッドを呼び出して、エントリ ポイント関数から返すポインターを使用してログオン プロセスを開始します。 このメソッドは、サービス プロバイダーの種類に応じて、次のように異なります。
  
- [IABProvider::アドレス帳](iabprovider-logon.md) プロバイダーのログオン 
    
- [IMSProvider::メッセージ ストア](imsprovider-logon.md) プロバイダーのログオン 
    
- [IXPProvider::トランスポート](ixpprovider-transportlogon.md) プロバイダーの TransportLogon 
    
実装するログオン方法で、次のタスクを実行します。
  
1. [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx)メソッドを呼び出して、入力パラメーターとして渡されるサポート オブジェクトの参照カウントを増やします。 
    
2. サポート オブジェクトの [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md) メソッドを呼び出して、プロファイル セクションにアクセスします。 
    
3. プロファイル セクションの [IMAPIProp::SetProps](imapiprop-setprops.md) メソッドを呼び出して、次のプロパティを設定します。 
    
  - **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))
    
  - **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))
    
  - **PR_PROVIDER_DISPLAY** ([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md))
    
  - **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))
    
  > [!NOTE]
  > プロファイル セクションのプロパティを設定したり、プロパティ **PR_RESOURCE_FLAGS PR_PROVIDER_DLL_NAME** したりしない。 ログオン時に、これらのプロパティは読み取り専用です。 
  
4. 構成に必要なプロパティがプロファイルに格納されている、またはユーザーが使用できるプロパティを確認します。 構成の確認の詳細については [、「Verifying Service Provider Configuration」を参照してください](verifying-service-provider-configuration.md)。
    
5. プロバイダーがアドレス帳またはメッセージ ストア プロバイダーである場合は、サポート オブジェクトの [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md) メソッドを呼び出して、一意の識別子 [(MAPIUID)](mapiuid.md)を登録します。 MAPI が [IXPLogon::AddressTypes](ixplogon-addresstypes.md)メソッドを呼び出す場合、トランスポート プロバイダーは **MAPIUID** 構造体を登録します。 **MAPIUID** の登録の詳細については、「Registering Service [Provider Unique IDENTIFIERs」を参照してください](registering-service-provider-unique-identifiers.md)。
    
6. ログオン オブジェクトをインスタンス化し、次のいずれかの値を返します。
    
  - S_OK正常にログオンされたことを示すメッセージが表示されます。
    
  - MAPI_E_UNCONFIGURED 1 つ以上の構成プロパティが使用できなかったかどうかを示します。
    
  - MAPI_E_USER_CANCELが構成ダイアログ ボックスをキャンセルし、構成プロパティが使用できないことを示します。
    
  - MAPI_E_FAILONEPROVIDERプロバイダーを構成できないが、MAPI で使用を許可する必要があります。 ログオン メソッドは、この値を返して、プロバイダーがパスワードを要求し、ユーザー インターフェイスが無効になっているため、ユーザーにメッセージを表示できない場合など、非fatal エラーを報告する必要があります。 
    
前のタスクの一覧では、サービス プロバイダーのログオン メソッドの最小実装について説明します。 必要に応じて、追加の機能を含めできます。 たとえば、一部のプロバイダーは [IMAPISupport::ModifyStatusRow](imapisupport-modifystatusrow.md) を呼び出して、ログオン メソッドで状態テーブルを更新します。 
  
> [!NOTE]
> ログオン時に最高のパフォーマンスを実現するには [、IMAPISupport::P repareSubmit](imapisupport-preparesubmit.md) または [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md)を呼び出さしないようにします。 これらの呼び出しを完了し、ログオン メソッドに制御を戻す前に、MAPI スプーラーを開始する必要があります。 
  
## <a name="see-also"></a>関連項目

- [サービス プロバイダーの開始](starting-a-service-provider.md)

