---
title: アドレス帳プロバイダーへのログオンとログオフの実装
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c4a1fb5d-ae23-445b-a6f0-ef430b03fc9a
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 1ffde0814fe5024a3f89a93462c48136712f1013
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800929"
---
# <a name="implementing-address-book-provider-logon-and-logoff"></a>アドレス帳プロバイダーへのログオンとログオフの実装

**適用されます**: Outlook 
  
アドレス帳プロバイダーのメソッドを実装することによってセッションのログオンとログオフをサポートする、 [IABProvider: IUnknown](iabprovideriunknown.md)インタ フェースです。 * * IABProvider * * インターフェイス**IUnknown**から直接継承し、他の 2 つの方法:**ログオン**と**シャット ダウン**します。 
  
## <a name="logoff"></a>ログオフ

MAPI は、プロバイダーが現在のプロファイルに追加し、クライアントは、動的再構成をサポートしているときに、すべてのセッションの冒頭に、プロバイダーの[IABProvider::Logon](iabprovider-logon.md)メソッドを呼び出します。 MAPI では、 **IABProvider::Logon**メソッドを呼び出して、アドレス帳プロバイダーは、ログオン プロセスを開始します。 
  
**IABProvider::Log を実装するには**
  
1. すべての MAPI によって渡される出力パラメーターのポインターを初期化します。 
    
2. サポート オブジェクトの**IUnknown::AddRef**メソッドを呼び出して、参照カウントをインクリメントします。 
    
3. サポート オブジェクトの[IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md)メソッドを呼び出して、プロバイダーの構成情報を含むプロファイルのセクションを開きます。 変更を加える場合は、 _lpUID_パラメーターと MAPI_MODIFY フラグの NULL を渡します。 
    
4. プロファイル セクションの[IMAPIProp::GetProps](imapiprop-getprops.md)メソッドを呼び出して、プロバイダーがデータ ファイルまたはデータベース テーブルの名前などのログオンの必要があるプロパティを取得します。 
    
5. プロパティは、すべて使用可能で有効なことを確認してください。 必要に応じて、許可されている場合は、無効なまたは不足している情報への追加や修正を行うし、メソッドを呼び出してプロファイル セクションの[IMAPIProp::SetProps](imapiprop-setprops.md)をすべての変更を保存するように求めるダイアログ ボックスを表示します。 使用可能にする必要がある一般的なプロパティの一部は次のとおりです。 
    
   **PR_DISPLAY_NAME**([PidTagDisplayName](pidtagdisplayname-canonical-property.md))
    
   **PR_ENTRYID**([PidTagEntryId](pidtagentryid-canonical-property.md))
    
   **PR_PROVIDER_DISPLAY**([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md))
    
   **PR_RECORD_KEY**([PidTagRecordKey](pidtagrecordkey-canonical-property.md))
    
   > [!NOTE]
   > **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) または**PR_PROVIDER_DLL_NAME** ([PidTagProviderDllName](pidtagproviderdllname-canonical-property.md)) は設定されていません。 ログオン時に、これらのプロパティは読み取り専用です。 
  
6. 1 つまたは複数の構成のプロパティが利用できない場合は失敗し、MAPI_E_UNCONFIGURED の値を返します。
    
7. の[MAPIUID](mapiuid.md)を登録するのには[IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md)を呼び出します。 プロバイダーによっては、 **MAPIUID**を作成できます。 
    
   - [IMAPISupport::NewUID](imapisupport-newuid.md)メソッドを呼び出しています。 
    
   - UUIDGEN を呼び出しています。EXE ツールを使用して、いずれかのヘッダー ファイルに含めるには、プロバイダーを使用する GUID を定義します。
    
8. 必要な場合を保存**MAPIUID**の新しく作成された現在のプロファイルのプロファイルのセクションを呼び出すことによって * * IMAPIProp::SetProps * * メソッドです。 
    
9. **** メソッドを呼び出すことによってプロファイル セクションをリリースします。 
    
10. 新しいログオン オブジェクトをインスタンス化し、この新しいオブジェクトのアドレスに、 _lppABLogon_パラメーターの内容を設定します。 
    
MAPI 呼び出しの可能性があるため、* * ログオン * * セッション中に何回かメソッド、複数のログオン オブジェクトを作成し、作成される各オブジェクトの追跡を維持することで、実装では、この可能性をサポートすることが賢明です。 **ログオン**の複数の呼び出しをサポートにより、クライアント アプリケーションのユーザーなどの異なるアイデンティティまたは使用して、別の配送先とのセッションにログオンします。 
  
**シャット ダウン**は、セッションが終了するときに呼び出されます。 MAPI メソッドを呼び出して、 [IABProvider::Shutdown](iabprovider-shutdown.md)最後のタスクの 1 つとして、セッションをシャット ダウンに関連します。 MAPI は、すべてのプロバイダーのログオン オブジェクトをリリースしましたし、最後の呼び出しを受信することがあると見なすことが、プロバイダーは、この呼び出しを受信するとします。 **IABProvider::Shutdown**の実装では、必要と思われる任意の最終的なクリーンアップを実行します。 などのセッションであるか、または解放するがまだ設定されているオブジェクトのメソッド**が**実行中にアイドル状態のエンジンを使用するのには**MAPIInitIdle**が呼び出される場合、プロバイダーでは**MAPIDeinitIdle**を呼び出す可能性があります。 
  
最終的なクリーンアップは、プロバイダーがない場合は、その実装を 1 行のコード変更できます。 
  
```cpp
return S_OK;

```


