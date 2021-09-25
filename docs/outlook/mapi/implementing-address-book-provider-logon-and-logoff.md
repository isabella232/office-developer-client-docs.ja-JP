---
title: アドレス帳プロバイダーのログオンとログオフの実装
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: c4a1fb5d-ae23-445b-a6f0-ef430b03fc9a
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 863fc2caa7bbe3586ba0fb99ad705a95270abf4a
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59575674"
---
# <a name="implementing-address-book-provider-logon-and-logoff"></a>アドレス帳プロバイダーのログオンとログオフの実装

**適用対象**: Outlook 2013 | Outlook 2016 
  
アドレス帳プロバイダーは [、IABProvider : IUnknown](iabprovideriunknown.md) インターフェイスのメソッドを実装することで、セッション のログオンとログオフをサポートします。 ** IABProvider ** インターフェイスは **IUnknown** から直接継承し、ログオンとシャットダウンの 2 つのメソッド **のみを** 追加 **します**。 
  
## <a name="logoff"></a>Logoff

MAPI は、すべてのセッションの開始時に、プロバイダーが現在のプロファイルに追加され、クライアントが動的再構成をサポートするたびに、プロバイダーの [IABProvider::Logon](iabprovider-logon.md) メソッドを呼び出します。 MAPI が **IABProvider::Logon** メソッドを呼び出す場合、アドレス帳プロバイダーはログオン プロセスを開始します。 
  
**IABProvider を実装するには::Log**
  
1. MAPI で渡された出力パラメーター ポインターのすべてを初期化します。 
    
2. サポート オブジェクトの **IUnknown::AddRef** メソッドを呼び出して、参照カウントを増やします。 
    
3. サポート オブジェクトの [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md) メソッドを呼び出して、プロバイダーに関する構成情報を含むプロファイルのセクションを開きます。 変更を行う  _場合は、lpUID_ パラメーター MAPI_MODIFYフラグに NULL を渡します。 
    
4. プロファイル セクションの [IMAPIProp::GetProps](imapiprop-getprops.md) メソッドを呼び出して、データ ファイルやデータベース テーブルの名前など、プロバイダーがログオンに必要なプロパティを取得します。 
    
5. すべてのプロパティが使用可能で有効なプロパティを確認します。 必要に応じて許可されている場合は、ダイアログ ボックスを表示して、無効または不足している情報に修正または追加を行い、プロファイル セクションの [IMAPIProp::SetProps](imapiprop-setprops.md) メソッドを呼び出して、変更を保存するようにユーザーに求めるメッセージを表示します。 使用できる一般的なプロパティには、次のようなものがあります。 
    
   **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))
    
   **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))
    
   **PR_PROVIDER_DISPLAY** ([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md))
    
   **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))
    
   > [!NOTE]
   > [PidTagResourceFlags](pidtagresourceflags-canonical-property.md) **)** または PR_RESOURCE_FLAGS ([PidTagProviderDllName](pidtagproviderdllname-canonical-property.md))**をPR_PROVIDER_DLL_NAME** 設定しない。 ログオン時に、これらのプロパティは読み取り専用です。 
  
6. 1 つ以上の構成プロパティが使用できない場合は、エラーが発生し、その値をMAPI_E_UNCONFIGURED。
    
7. [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md)を呼び出して[MAPIUID を登録します](mapiuid.md)。 プロバイダーは、次の **方法で MAPIUID を作成** できます。 
    
   - [IMAPISupport::NewUID メソッドを呼び出](imapisupport-newuid.md)します。 
    
   - プロバイダーがUUIDGEN.EXEファイルに含める GUID を定義するために、このツールを呼び出します。
    
8. 必要に応じて、プロファイル セクションの ** IMAPIProp::SetProps ** メソッドを呼び出して、新しく作成した **MAPIUID** を現在のプロファイルに保存します。 
    
9. プロファイル セクションを解放するには **、IUnknown::Release メソッドを呼び出** します。 
    
10. 新しいログオン オブジェクトをインスタンス化し  _、lppABLogon_ パラメーターの内容をこの新しいオブジェクトのアドレスに設定します。 
    
MAPI はセッション中に ** Logon ** メソッドを複数回呼び出す可能性があるから、複数のログオン オブジェクトを作成し、作成された各オブジェクトを追跡することで、実装でこの可能性をサポートする方が賢明です。 複数の **ログオン呼び** 出しをサポートすると、クライアント アプリケーションのユーザーは、たとえば、異なる ID を持つセッションにログオンしたり、異なる配信先を使用したりできます。 
  
**セッション** の終了時にシャットダウンが呼び出されます。 MAPI は、セッションのシャットダウンに関連する最後のタスクの 1 つとして [、IABProvider::Shutdown](iabprovider-shutdown.md) メソッドを呼び出します。 MAPI は、プロバイダーのすべてのログオン オブジェクトを解放し、プロバイダーがこの呼び出しを受信すると、これが最後に受信する呼び出しと見なす可能性があります。 **IABProvider::Shutdown** の実装では、必要と思う最終クリーンアップを実行します。 たとえば、セッション中にアイドル エンジンを使用するために **MAPIInitIdle** を呼び出した場合、プロバイダーは **MAPIDeinitIdle** を呼び出したり、まだリリースされていないオブジェクトの **IUnknown::Release** メソッドを呼び出したりします。 
  
プロバイダーに最終的なクリーンアップがない場合、その実装は 1 行のコードで構成できます。 
  
```cpp
return S_OK;

```


