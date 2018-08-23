---
title: MAPI の関数へのリンクします。
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: be72a893-a3bc-4dea-8234-47f3e1db4515
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 5cb791d0d350a04864191a0a9d35a2f1c8b165d7
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22577717"
---
# <a name="link-to-mapi-functions"></a>MAPI の関数へのリンクします。

**適用されます**: Outlook 2013 |Outlook 2016 
  
リンクの 3 つの方法があります: 暗黙的なリンク、明示的なリンク、および MAPI スタブ ライブラリを使用して新しいハイブリッド モデルです。
  
## <a name="implicit-linking"></a>暗黙的なリンク

従来、メッセージング アプリケーションでは常に MAPI の関数を呼び出すと関与 Mapi32.lib ライブラリへのリンクです。 これには、Mapi32.dll で、実行時に既定の MAPI クライアント実装への呼び出しを転送し、Windows の MAPI スタブ ライブラリにルーティングの MAPI 呼び出しが含まれています。 この呼び出しプロセスは、暗黙的なリンクと呼びます。 次の図の左側には、MAPI の関数の呼び出しプロセスで使用されている暗黙的なリンクの例を示します。 プロセスは、MAPI アプリケーションによって開始されますと MAPI ライブラリ (Mapi32.lib) と Windows の MAPI スタブ (Mapi32.dll) し、MAPI スタブ (Msmapi32.dll) の Outlook MAPI クライアントの実装が完了しました。
  
**暗黙的および明示的なリンクの比較を行います。**

![暗黙的および明示的なリンクの比較](media/09d9c49a-a52d-4407-9013-d0d14c8f63f6.gif "暗黙的および明示的なリンクの比較")
  
## <a name="explicit-linking"></a>明示的なリンク

既定の MAPI クライアントは、Windows インストーラー (MSI) を使用して、オンデマンド インストールをサポートするため、MAPI ライブラリを使用するのではなく Outlook MAPI スタブと Windows の MAPI スタブに直接メッセージング ・ アプリケーションを開発できます。 前の図の右側には、(手順 2 を次のセクションで)、Outlook MAPI スタブの DLL の名前とパスを検索し、関数の呼び出しに、Outlook MAPI スタブ (は、MAPI アプリケーションを最初から、MAPI の関数の呼び出しプロセスの例を示しています。手順 3 で次のセクション)。 次の手順では、明示的なリンクを使用して MAPI の関数を呼び出す方法を示します。 
  
> [!NOTE]
> 明示的なリンクについては、次のセクションで説明した MAPIStubLibrary.lib の導入に伴い、お客様のニーズに不要な可能性があります。 暗黙のモデルでは、ような新しいライブラリがすべてを管理し、Outlook に必要な明示的なリンクのロジックを実装する MAPI を直接します。 
  
明示的リンクの詳細については、明示的にリンク参照してください。
  
### <a name="to-call-mapi-api-elements-without-the-mapi-library-and-the-windows-mapi-stub"></a>MAPI ライブラリと Windows の MAPI スタブのない MAPI API 要素を呼び出す

1. プログラム ファイルで使用している MAPI API 要素ごとに関数ポインターのグローバル リストを作成します。 
    
   次の例では、この手順を示します。
    
   ```cpp
    //Global MAPI function pointers
    LPMAPIINITIALIZE pfnMAPIInitialize = NULL;
    LPMAPIUNINITIALIZE pfnMAPIUninitialize = NULL;
   ```

2. 既定の MAPI クライアント (たとえば、Msmapi32.dll の Microsoft Outlook の MAPI DLL にリンクするのには MAPI の関数を初期化する関数を作成します。 この関数では、次の操作を行います。 
    
    1. システムの適切なディレクトリから mapi32.dll をロードします。 
        
       |||
       |:-----|:-----|
       |x64 または x86 でネイティブに  <br/> |**%windir%\system32\mapi32.dll** <br/> |
       |WoW モードでの x86  <br/> |**%windir%\syswow64\mapi32.dll** <br/> |
    
    2. MAPI のサブシステムを実装する DLL の名前とパスを取得する[FGetComponentPath](fgetcomponentpath.md)関数を呼び出します。 詳細については、[特定のバージョンの MAPI 負荷の選択](how-to-choose-a-specific-version-of-mapi-to-load.md)を参照してください。
        
    3. LoadLibrary 関数を呼び出すことによって、DLL を読み込みます。 
        
    4. GetProcAddress 関数を呼び出すことによって、MAPI の関数ポインターの配列を初期化します。 
        
    次の使用例は、上記の手順を示しています。
        
   ```cpp
    void InitializeMapiFunctions()
    {
    {
        // Get the DLL path and name of the actual MAPI implementation.
        FGetComponentPath(g_szMapiComponentGUID, NULL, szMAPIDLL, MAX_PATH);
        // Load the DLL.
        hMod = LoadLibrary(szMAPIDLL);
        // Initialize MAPI functions.
        pfnMAPIInitialize = GetProcAddress(hMod, "MAPIInitialize");
        pfnMAPIUninitialize = GetProcAddress(hMod, "MAPIUninitialize");
    }
   ```

3. 最後に、MAPI API 要素への呼び出しを行う前に、手順 2 では、メッセージング アプリケーションの作成の場合にこの関数を呼び出します。 
    
   > [!CAUTION]
   > アプリケーションを閉じる前に、MAPI サブシステムの初期化を解除する必要があります。 
  
   次の使用例は、この手順を示しています。 
    
   ```cpp
    int main()
    {
        HRESULT hr;
        InitializeMapiFunctions();
        // Initialize the MAPI subsystem.
        hr = (*pfnMAPIInitialize)(NULL);
        if (hr!= S_OK)
        {
            // Handle the error case.
        }
        // Here is where you make calls to other MAPI interfaces.
        // Uninitialize the MAPI subsystem.
        (*pfnMAPIUninitialize)();
    return (0);
    }
   ```

## <a name="mapistublibrarylib"></a>MAPIStubLibrary.lib

Microsoft Outlook 2010 と 64 ビットの MAPI、Microsoft Outlook 2013 年に拡張するようになりましたの登場は従来の 32 ビット API の完全な実装です。 新しいプロジェクト、MAPI スタブ ライブラリでは、CodePlex の web サイトに掲載は、32 ビットと 64 ビットの両方の MAPI アプリケーションの構築をサポートする Mapi32.lib のドロップイン交換を提供します。 MAPIStubLibrary.lib で MAPI を明示的にリンクする必要があるし、ことを構築することからを削除する Mapi32.lib、リンカーの設定では、MAPIStubLibrary.lib に置き換えることコードにさらに変更は必要ありません。 Mapi32.lib で、明示的なリンクを使用する場合が必要ではありませんが、このライブラリ ファイル内に含まれている最新のエクスポートを処理するために**LoadLibrary**と**GetProcAddress**を**終わった**のコードを記述する必要もなくなります。 
  
Mapi32.lib では使用できませんが、このライブラリにリンクしている新しい機能の一部を以下に示します。
  
- [GetDefCachedMode](getdefcachedmode.md)    
- [HrGetGALFromEmsmdbUID](hrgetgalfromemsmdbuid.md)   
- [HrOpenOfflineObj](hropenofflineobj.md)    
- [MAPICrashRecovery](mapicrashrecovery.md)   
- [OpenStreamOnFileW](openstreamonfilew.md)    
- [WrapCompressedRTFStreamEx](wrapcompressedrtfstreamex.md)
    
MAPI スタブ ライブラリを組み込むことの別の方法は、プロジェクトに直接、MapiStubLibrary.cpp、StubUtils.cpp、ソース ファイルをコピーし、Mapi32.lib へのリンケージ、および MAPI に明示的にリンクする任意のコードを削除することです。
  
MAPI スタブ ライブラリのファイルにアクセスし、ビルドし、統合のプロジェクトと同様にこのライブラリについての質問に次のようにタイミングと理由についての情報を使用してを参照してください[MAPI スタブ ライブラリ](http://mapistublibrary.codeplex.com/documentation)CodePlex サイトです。 
  
## <a name="see-also"></a>関連項目

- [MAPI �v���O���~���O�̊T�v](mapi-programming-overview.md)
- [MAPI サブシステムのインストール](installing-the-mapi-subsystem.md)
- [MAPI ヘッダー ファイルをインストールする](how-to-install-mapi-header-files.md)
- [読み込む MAPI の特定のバージョンを選択する](how-to-choose-a-specific-version-of-mapi-to-load.md)
- [使用するリンク方式の使い分け](http://msdn.microsoft.com/en-us/library/253b8k2c.aspx)
- [実行可能ファイルを DLL にリンクします。](http://msdn.microsoft.com/en-us/library/9yd93633.aspx)
- [MAPI DLL の MSI のキーの設定](http://msdn.microsoft.com/en-us/library/ee909494%28v=VS.85%29.aspx)

