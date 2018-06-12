---
title: Windows ユニバーサル アプリからの Office との統合
manager: soliver
ms.date: 02/06/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 60b4fa23-0075-4f6a-8bd0-9e53e99432d5
description: Windows ユニバーサル アプリ プラットフォームのサードパーティ アプリを Excel Mobile、PowerPoint Mobile、Word Mobile と統合できます。ユニバーサル アプリを Office アプリと統合する際には、Windows ファイル ピッカー コントラクト、expando プロパティ、キャッシュ ファイル更新プログラム コントラクト を使います。
ms.openlocfilehash: 2c170fd55c9c6f10d348610ffbc75ffa86447529
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799229"
---
# <a name="integrate-with-office-from-windows-universal-apps"></a>Windows ユニバーサル アプリからの Office との統合

Windows ユニバーサル アプリ プラットフォームのサードパーティ アプリを Excel Mobile、PowerPoint Mobile、Word Mobile と統合できます。ユニバーサル アプリを Office アプリと統合する際には、Windows [ファイル ピッカー コントラクト](https://msdn.microsoft.com/en-us/library/windows/apps/hh465174.aspx)、[expando プロパティ](https://msdn.microsoft.com/en-us/library/windows/apps/xaml/hh770655.aspx)、[キャッシュ ファイル更新プログラム コントラクト](https://msdn.microsoft.com/en-us/library/windows/apps/windows.storage.provider.cachedfileupdater.aspx) を使います。
  
ユニバーサル アプリを Excel、PowerPoint、または Word Mobile と統合すると、ユーザーはそのアプリで提供されている Office ドキュメントを開くことができます。これは Office 内から閲覧するときにも、Windows を使用してそのアプリ内からファイルを開くときにも当てはまります。ユーザーがユニバーサル アプリにファイルを再び保存し、そのアプリからご使用のサービスにファイルをアップロードすることもできます。
  
この方法で開いたファイルは Office の最近使用したファイルの一覧に表示されるので、ユーザーは簡単に検索して再び開くことができます。
  
この統合を行うには、ユニバーサル アプリが以下の条件を満たしている必要があります。
    
- Windows [ファイル ピッカー コントラクト](https://msdn.microsoft.com/en-us/library/windows/apps/hh465174.aspx)を実装している。
    
- ファイル ストア (クラウド ストレージにアクセスできるアプリなど) を表している。
    
## <a name="expando-properties"></a>Expando プロパティ

Windows ユニバーサル アプリは、Expando プロパティを使用して、ファイルに関連付けられている追加情報を伝達できます。Windows でのこの操作の流れについては、「[StorageItemContentProperties.SavePropertiesAsync](https://msdn.microsoft.com/en-us/library/windows/apps/xaml/hh770655.aspx)」の「System.ExpandoProperties」を参照してください。
  
次の表に、ファイルを開くシナリオが有効になるように、アプリから Office に提供する必要があるプロパティを示します。この情報を提供しないと、アプリからのファイルはすべて読み取り専用として開かれます。ユーザーが編集の目的でファイルを開くことができるかどうかは、ユーザーが持つ Office ライセンスの種類と、ユーザーが開こうとしているドキュメントの種類に応じて異なります。
  
これらのプロパティは、 **System.ExpandoProperties** プロパティ セット内で設定してください。 
  
|**プロパティ**|**説明**|**型**|**例**|
|:-----|:-----|:-----|:-----|
|**AppDisplayName** <br/> |ユーザーに対して表示するプロバイダー名。Office では、最近使用したドキュメントの一覧などの複数の場所に表示されます。  <br/> |文字列型 (String)  <br/> |Contoso  <br/> |
|**MicrosoftOfficeOwnershipType** <br/> |ライセンスの場合、ドキュメント/場所が Personal/Consumer か Work/Business かを示します。使用できる値は 1 (Personal) と 2 (Business) です。たとえば、ユーザーのファイルが Contoso Business に保存される場合は Business の値「2」を使用します。  <br/> |Unit32  <br/> | 1 または 2  <br/> たとえば、ユーザーのファイルが Contoso Business に保存される場合は、このファイルに Business の「2」のマークを付ける必要があります。  <br/> |
|**MicrosoftOfficeTermsOfUse** <br/> |提供した情報が利用規約どおりに正確であることを宣言する法的な文章。このテキストはユーザーに対しては表示されません。ご自分とアプリケーションのプロバイダーと Microsoft の間の同意になります。  <br/> 例については、以下をご覧ください。  <br/> | 文字列  <br/> | [https://go.microsoft.com/fwlink/p/?LinkId=528381](third-party-applications-integrating-with-office-mobile-products.md) にある条項に同意します。 <br/> |
   
次のコード例は、これらのプロパティを設定する方法を示しています。
  
```cs
public static async Task SetExpandoProperties(StorageFile file,... other params ...) 
  { 
     var expandoProperties = new PropertySet(); 
     expandoProperties.Add("AppDisplayName", "Contoso",);  
     // String value. 
     expandoProperties.Add("MicrosoftOfficeOwnershipType", 1);  
     // Unit32 value - 1 (for personal), 2 (for business).  
     expandoProperties.Add("MicrosoftOfficeTermsOfUse", "I agree to the terms located at https://go.microsoft.com/fwlink/p/?LinkId=528381");   
    // String value. 
          
       var fileProperties = new PropertySet(); 
       fileProperties.Add("System.ExpandoProperties", expandoProperties); 
       await file.Properties.SavePropertiesAsync(fileProperties); 
  } 

```

## <a name="cached-file-updater-contracts"></a>キャッシュ ファイル更新プログラム コントラクト

ユニバーサル アプリがキャッシュ ファイル更新プログラム コントラクトに参加すると、別のユニバーサル アプリ (Office など) からファイルに加えられた変更が通知されます。Windows でのこの操作の流れについては、「[CachedFileUpdater Class ](https://msdn.microsoft.com/en-us/library/windows/apps/windows.storage.provider.cachedfileupdater.aspx)」を参照してください。
  
Office は **AllowOnlyReaders** オプションを使用して、ユニバーサル アプリからファイル ピッカー コントラクトを通じて提供された読み取り/書き込みファイルを開きます。したがって、Office でファイルが開かれている間は、独自のアプリなどの別のアプリで移動、削除、名前変更、書き込みを行うことはできません。 Office はファイルを自動保存しますが、CachedFileManager.DeferUpdates を設定して、Office でドキュメントが閉じられるか Windows によって Office が中断される (ユーザーが別のアプリに切り替えた時点) までアプリがアクティブにならないようにします。Office がファイルを閉じると、アプリでこれに書き込みができるようになります。 
  
ダウンロード、更新、アップロードを含む、サービスとのすべての通信をアプリで処理する必要があります。
  
次の表に、アプリと Office の間の相互作用を処理する場合に設定するパラメーターの一覧を示します。
  
|**パラメーター**|**説明**|
|:-----|:-----|
|[ReadActivationMode](https://msdn.microsoft.com/en-us/library/windows/apps/windows.storage.provider.readactivationmode.aspx) <br/> |ファイルを Office に送信する前にアプリで更新できるようにするには、 **BeforeAccess** を設定します。  <br/> |
|[WriteActivationMode](https://msdn.microsoft.com/en-us/library/windows/apps/windows.storage.provider.writeactivationmode.aspx) <br/> |ファイルを読み取り専用にするには、 **ReadOnly** を設定します。Office でのファイルの処理が終わったら CacheFileUpdater によってアプリが起動されるようにするには、 **AfterWrite** を設定します。  <br/><br/>**注**: **AfterWrite**が設定されていない場合、アプリケーションは通知されません、変更をアップロードするユーザーの変更がローカルのみすることを意味します。           |
|[CachedFileOptions.RequireUpdateOnAccess](https://msdn.microsoft.com/en-us/library/windows/apps/windows.storage.provider.cachedfileoptions.aspx) <br/> |最近使用したファイルの一覧からユーザーがファイルにアクセスする際に、アプリがファイルを更新できるようにするには、このプロパティを設定します。  <br/> |
   
## <a name="invoking-office-from-your-app"></a>アプリからの Office の呼び出し

ユーザーがアプリから Office ドキュメントを開く際には、Excel Mobile、PowerPoint Mobile、Word Mobile でそのドキュメントを開くことができます。たとえば、ユーザーがアプリで \*.docx ファイルを選択すると、Word Mobile が起動して \*.docx ファイルが開き ます。どの Office アプリで開くかは、ユーザーがどのアプリをそのファイルの種類に関連付けているかに応じて異なります。
  
Office でアプリからのファイルを開くには、 **LaunchFileAsync()** を使用してファイルを起動することをお勧めします。 **LaunchUriAsync()** を使用してファイルを起動することはお勧めしません。Office ではなく、URI スキーマ用に登録されたアプリケーション (ブラウザー) が起動するからです。 **LaunchUriAsync()** に **LauncherOptions.ContentType()** オプションを指定して Office を呼び出すこともできますが、この場合は、開かれるファイルに一時ファイルのマークが付けられ、Office で読み取り専用になります。 
  
詳細については、「[Launcher クラス](https://msdn.microsoft.com/en-us/library/windows/apps/windows.system.launcher.aspx)」を参照してください。
  
## <a name="temporary-and-read-only-files"></a>一時ファイルと読み取り専用ファイル

アプリ内で、一時ファイルに対して **FILE_ATTRIBUTE_TEMPORARY** 属性を設定し、読み取り専用ファイルに対して **FILE_ATTRIBUTE_READONLY** 属性を設定します。 
  
**FILE_ATTRIBUTE_TEMPORARY** 属性や **FILE_ATTRIBUTE_READONLY** 属性が設定されたファイルは、Office で読み取り専用として開かれます。また **FILE_ATTRIBUTE_TEMPORARY** は、最近使用したファイルの一覧にファイルが表示されないようにします。 
  
ファイル属性の詳細については、「[SetFileAttributes 関数](https://msdn.microsoft.com/en-us/library/windows/desktop/aa365535%28v=vs.85%29.aspx)」を参照してください。
  
## <a name="other-best-practices"></a>その他のベスト プラクティス

競合する編集やエラーが発生した場合などにファイルの整合性を最適化するには、以下のベスト プラクティスを適用します。
  
- 保存が競合しないようにします。
    
  - サーバーの競合が発生した場合は、アップロードを一時停止して分岐しないようにします (分岐は、Office で開いている書き込みファイルがなくなった場合にのみ発生します)。通常、Office でアプリからのファイルを開くと、Office が閉じるか Windows によって中断される場合のみアプリがアクティブになります。
    
  - 競合を処理するための UI が必要な場合は、トースト通知を実装します。 Office が中断しているときには、完全な UI は使用できません。
    
- エラーを処理します。
    
  - ロックが解除されると、ユーザーに競合が通知され、アプリ内でそれを解決するためのパスが提供されます。
    
## <a name="see-also"></a>関連項目

- [Office との統合](integrate-with-office.md)   
- [Win32 同期クライアントからの Office との統合](integrate-with-office-from-win32-sync-clients.md)
    

