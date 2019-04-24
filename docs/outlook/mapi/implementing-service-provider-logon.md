---
title: サービスプロバイダーログオンの実装
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 3d3c309f-fe60-43a9-beda-16b09ec769db
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 533c00a0c994e7dfc5adc476899553bc39a2a9ab
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310088"
---
# <a name="implementing-service-provider-logon"></a>サービスプロバイダーログオンの実装

**適用対象**: Outlook 2013 | Outlook 2016 
  
MAPI は、エントリポイント関数から返されるポインターを使用してログオンプロセスを開始するために、プロバイダオブジェクト内のメソッドを呼び出します。 このメソッドは、サービスプロバイダーの種類に応じて、次のように異なります。
  
- [IABProvider::](iabprovider-logon.md)アドレス帳プロバイダーのログオン 
    
- [IMSProvider::](imsprovider-logon.md)メッセージストアプロバイダーへのログオン 
    
- [ixpprovider::](ixpprovider-transportlogon.md)トランスポートプロバイダーの transportlogon 
    
実装する任意のログオン方法で、次のタスクを実行します。
  
1. 入力パラメーターとして渡される support オブジェクトの参照カウントをインクリメントするには、 [IUnknown:: AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx)メソッドを呼び出します。 
    
2. サポートオブジェクトの[imapisupport:: openprofilesection](imapisupport-openprofilesection.md)メソッドを呼び出して、プロファイルセクションにアクセスします。 
    
3. プロファイルセクションの[imapiprop:: setprops](imapiprop-setprops.md)メソッドを呼び出して、次のプロパティを設定します。 
    
  - **PR_DISPLAY_NAME**([PidTagDisplayName](pidtagdisplayname-canonical-property.md))
    
  - **PR_ENTRYID**([PidTagEntryId](pidtagentryid-canonical-property.md))
    
  - **PR_PROVIDER_DISPLAY**([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md))
    
  - **PR_RECORD_KEY**([PidTagRecordKey](pidtagrecordkey-canonical-property.md))
    
  > [!NOTE]
  > プロファイルセクションの**PR_RESOURCE_FLAGS**プロパティまたは**PR_PROVIDER_DLL_NAME**プロパティを設定しようとしないでください。 ログオン時に、これらのプロパティは読み取り専用になります。 
  
4. 構成に必要なプロパティがプロファイルに保存されているか、ユーザーから使用可能であることを確認してください。 構成の確認の詳細については、「[サービスプロバイダーの構成を確認](verifying-service-provider-configuration.md)する」を参照してください。
    
5. サポートオブジェクトの[imapisupport:: setprovideruid](imapisupport-setprovideruid.md)メソッドを呼び出して、プロバイダーがアドレス帳またはメッセージストアプロバイダーの場合は、一意の識別子 ( [MAPIUID](mapiuid.md)) を登録します。 トランスポートプロバイダーは、MAPI が[IXPLogon:: AddressTypes](ixplogon-addresstypes.md)メソッドを呼び出すときに、 **MAPIUID**構造体を登録します。 **MAPIUID**の登録の詳細については、「[サービスプロバイダーの一意識別子の登録](registering-service-provider-unique-identifiers.md)」を参照してください。
    
6. ログオンオブジェクトをインスタンス化し、次のいずれかの値を返します。
    
  - 成功したログオンを示す S_OK。
    
  - MAPI_E_UNCONFIGURED は、1つ以上の構成プロパティが使用できないことを示します。
    
  - MAPI_E_USER_CANCEL は、ユーザーが構成ダイアログボックスをキャンセルし、構成プロパティが使用できなくなったことを示します。
    
  - MAPI_E_FAILONEPROVIDER は、プロバイダーを構成できないが、MAPI が使用できるようにする必要があることを示します。 ログオン方法では、プロバイダーがパスワードを必要とする場合や、ユーザーインターフェイスが無効になっているためユーザーにメッセージを表示できない場合など、致命的ではないエラーを報告するために、この値を返します。 
    
前述のタスクの一覧では、サービスプロバイダーログオン方法の最小実装について説明します。 必要に応じて、追加機能を含めることができます。 たとえば、一部のプロバイダーは[imapisupport:: modifystatusrow](imapisupport-modifystatusrow.md)を呼び出して、ログオン方法の状態テーブルを更新します。 
  
> [!NOTE]
> ログオン時に最高のパフォーマンスを得るには、 [imapisupport::P reparesubmit](imapisupport-preparesubmit.md)または[imapisupport:: SpoolerNotify](imapisupport-spoolernotify.md)のいずれかを呼び出すことを避けてください。 これらの呼び出しを完了して、ログオン方法に制御を戻す前に、MAPI スプーラーを開始する必要があります。 
  
## <a name="see-also"></a>関連項目

- [サービスプロバイダーの開始](starting-a-service-provider.md)

