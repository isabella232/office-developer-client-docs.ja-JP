---
title: アドレス帳プロバイダーのログオンとログオフの実装
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c4a1fb5d-ae23-445b-a6f0-ef430b03fc9a
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 8d33bccdd01075d692e5a887082ba51ee23bb083
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332929"
---
# <a name="implementing-address-book-provider-logon-and-logoff"></a>アドレス帳プロバイダーのログオンとログオフの実装

**適用対象**: Outlook 2013 | Outlook 2016 
  
アドレス帳プロバイダーは、 [IABProvider: IUnknown](iabprovideriunknown.md)インターフェイスのメソッドを実装することによって、セッションのログオンとログオフをサポートします。 * * IABProvider * * インターフェイスは**IUnknown**から直接継承し、次の2つのメソッドを追加します。**ログオン**と**シャットダウン**。 
  
## <a name="logoff"></a>Logoff

MAPI は、プロバイダーの[IABProvider:: Logon](iabprovider-logon.md)メソッドをすべてのセッションの開始時に呼び出し、プロバイダーが現在のプロファイルに追加され、クライアントが動的再構成をサポートするようになります。 MAPI が**IABProvider:: logon**メソッドを呼び出すと、アドレス帳プロバイダーのログオンプロセスが開始されます。 
  
**IABProvider:: Log を実装するには**
  
1. MAPI によって渡されたすべての出力パラメータポインターを初期化します。 
    
2. サポートオブジェクトの**IUnknown:: AddRef**メソッドを呼び出して、参照カウントをインクリメントします。 
    
3. サポートオブジェクトの[imapisupport:: openprofilesection](imapisupport-openprofilesection.md)メソッドを呼び出して、プロバイダーに関する構成情報を含むプロファイルのセクションを開きます。 変更を行う予定がある場合は、 _lpuid_パラメーターと MAPI_MODIFY フラグに NULL を渡します。 
    
4. プロファイルセクションの[imapiprop:: GetProps](imapiprop-getprops.md)メソッドを呼び出して、プロバイダーがログオンに必要とするプロパティ (データファイルやデータベーステーブルの名前など) を取得します。 
    
5. プロパティがすべて使用可能で有効であることを確認してください。 必要であり、許可されている場合は、ユーザーに無効な情報や不足している情報を修正または追加するように求めるダイアログボックスを表示し、プロファイルセクションの[imapiprop:: setprops](imapiprop-setprops.md)メソッドを呼び出して変更を保存します。 利用できるようにする必要がある一般的なプロパティのいくつかを次に示します。 
    
   **PR_DISPLAY_NAME**([PidTagDisplayName](pidtagdisplayname-canonical-property.md))
    
   **PR_ENTRYID**([PidTagEntryId](pidtagentryid-canonical-property.md))
    
   **PR_PROVIDER_DISPLAY**([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md))
    
   **PR_RECORD_KEY**([PidTagRecordKey](pidtagrecordkey-canonical-property.md))
    
   > [!NOTE]
   > **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) または**PR_PROVIDER_DLL_NAME** ([PidTagProviderDllName](pidtagproviderdllname-canonical-property.md)) を設定しないでください。 ログオン時に、これらのプロパティは読み取り専用になります。 
  
6. 1つ以上の構成プロパティが使用できない場合は、エラーが発生し、MAPI_E_UNCONFIGURED 値が返されます。
    
7. [MAPIUID](mapiuid.md)を登録するには、呼び出し[imapisupport:: setprovideruid](imapisupport-setprovideruid.md)を呼び出します。 プロバイダーは、次の方法で**MAPIUID**を作成できます。 
    
   - [imapisupport:: newuid](imapisupport-newuid.md)メソッドを呼び出しています。 
    
   - UUIDGEN を呼び出しています。EXE ツールを使用して、プロバイダーがヘッダーファイルの1つに含める GUID を定義します。
    
8. 必要に応じて、プロファイルセクションの * * imapiprop:: setprops * * メソッドを呼び出して、新しく作成した**MAPIUID**を現在のプロファイルに保存します。 
    
9. **IUnknown:: release**メソッドを呼び出して、プロファイルセクションを解放します。 
    
10. 新しいログオンオブジェクトをインスタンス化し、 _lppablogon_パラメーターの内容をこの新しいオブジェクトのアドレスに設定します。 
    
セッション中に MAPI が * * Logon * * メソッドを何度も呼び出すことができるため、複数のログオンオブジェクトを作成し、作成された各オブジェクトを追跡できるように、実装でこの可能性をサポートすることをお勧めします。 複数の**ログオン**呼び出しをサポートすることにより、クライアントアプリケーションのユーザーは、異なる id を使用してセッションにログオンしたり、別の配信先を使用したりすることができます。 
  
**Shutdown**は、セッションが終了するときに呼び出されます。 MAPI は、セッションのシャットダウンに関連する最後のタスクの1つとして[IABProvider:: Shutdown](iabprovider-shutdown.md)メソッドを呼び出します。 MAPI では、プロバイダーのすべてのログオンオブジェクトが解放され、プロバイダーがこの呼び出しを受信するときに、これが最後に受信する呼び出しであると想定できます。 **IABProvider:: Shutdown**の実装で、必要と思われる最終的なクリーンアップを実行します。 たとえば、プロバイダーが**MAPIInitIdle**を呼び出し、セッション中にアイドル状態のエンジンを使用する場合、またはまだ解放されていないオブジェクトの**IUnknown:: Release**メソッドを呼び出した場合、 **MAPIDeinitIdle**を呼び出すことができます。 
  
プロバイダーが最終的なクリーンアップを行わない場合は、次の1行のコードでその実装を構成できます。 
  
```cpp
return S_OK;

```


