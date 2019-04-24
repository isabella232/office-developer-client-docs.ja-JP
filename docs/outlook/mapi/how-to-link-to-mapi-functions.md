---
title: MAPI 機能へのリンク
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: be72a893-a3bc-4dea-8234-47f3e1db4515
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 71108da8bb9914bb7ed0ad0b3adacc24e1d69e63
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346885"
---
# <a name="link-to-mapi-functions"></a>MAPI 機能へのリンク

**適用対象**: Outlook 2013 | Outlook 2016 
  
MAPI スタブライブラリを使用した暗黙的なリンク、明示的なリンク、新しいハイブリッドモデルのリンクには、次の3つの方法があります。
  
## <a name="implicit-linking"></a>暗黙的リンク

従来、メッセージングアプリケーションで MAPI 関数を呼び出すと、Mapi32 ライブラリへのリンクが常に必要になります。 これには、mapi 呼び出しを Windows mapi スタブライブラリ (Mapi32) にルーティングすると、実行時に既定の mapi クライアント実装に呼び出しが転送されます。 この呼び出しプロセスは暗黙的リンクと呼ばれます。 次の図の左側は、MAPI 関数呼び出しプロセスで使用される暗黙的リンクの例を示しています。 プロセスは mapi アプリケーションによって開始され、mapi ライブラリ (Mapi32) と Windows mapi スタブ (Mapi32) が含まれており、mapi スタブ (Msmapi32) の Outlook mapi クライアント実装によって完了します。
  
**暗黙的リンクと明示的なリンクの比較。**

![暗黙的リンクと明示的リンクの比較](media/09d9c49a-a52d-4407-9013-d0d14c8f63f6.gif "暗黙的リンクと明示的リンクの比較")
  
## <a name="explicit-linking"></a>明示的なリンク

既定の mapi クライアントは、windows インストーラー (MSI) を使用してオンデマンドインストールをサポートしているため、mapi ライブラリおよび Windows mapi スタブを使用する代わりに、Outlook mapi スタブ上にメッセージングアプリケーションを直接開発できます。 前の図の右側は mapi 関数呼び出しプロセスの例を示しています。 mapi アプリケーションでは、outlook mapi スタブのパスと DLL 名 (次のセクションの手順2を参照) を探し、outlook mapi スタブに関数呼び出しを行います (次のセクションの手順3を参照してください)。 次の手順は、明示的なリンクを使用して MAPI 機能を呼び出す方法を示しています。 
  
> [!NOTE]
> この情報は、次のセクションで説明されている MAPIStubLibrary の導入によって、必要に応じて明示的なリンクに関連している場合があります。 暗黙のモデルと同様に、新しいライブラリはすべてを管理し、Outlook の MAPI を直接読み込む明示的なリンクロジックを実装します。 
  
明示的リンクの詳細については、「明示的なリンク」を参照してください。
  
### <a name="to-call-mapi-api-elements-without-the-mapi-library-and-the-windows-mapi-stub"></a>mapi ライブラリおよび Windows mapi スタブを使用せずに mapi API 要素を呼び出すには

1. プログラムファイルで、使用している MAPI API 要素ごとに関数ポインターのグローバルリストを作成します。 
    
   次の例は、この手順を示しています。
    
   ```cpp
    //Global MAPI function pointers
    LPMAPIINITIALIZE pfnMAPIInitialize = NULL;
    LPMAPIUNINITIALIZE pfnMAPIUninitialize = NULL;
   ```

2. mapi 機能を初期化する関数を作成し、既定の mapi クライアント (たとえば、Microsoft Outlook の Msmapi32) の mapi DLL にリンクします。 この関数では、次の操作を行います。 
    
    1. 適切なシステムディレクトリから mapi32 を読み込みます。 
        
       |||
       |:-----|:-----|
       |x64 または x86 ネイティブ  <br/> |**%windir%\system32\mapi32.dll** <br/> |
       |WoW モードの x86  <br/> |**%windir%\syswow64\mapi32.dll** <br/> |
    
    2. [FGetComponentPath](fgetcomponentpath.md)関数を呼び出して、MAPI サブシステムを実装するパスと DLL 名を取得します。 詳細については、「[特定のバージョンの MAPI を読み込む」](how-to-choose-a-specific-version-of-mapi-to-load.md)を参照してください。
        
    3. LoadLibrary 関数を呼び出して DLL を読み込みます。 
        
    4. GetProcAddress 関数を呼び出して MAPI 関数ポインター配列を初期化します。 
        
    次の例は、前の手順を示しています。
        
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

3. 最後に、MAPI API 要素の呼び出しを行う前に、メッセージングアプリケーションの手順2で作成した関数を呼び出します。 
    
   > [!CAUTION]
   > アプリケーションを閉じる前に、MAPI サブシステムを初期化解除する必要があります。 
  
   次の例は、この手順を示しています。 
    
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

## <a name="mapistublibrarylib"></a>MAPIStubLibrary

microsoft outlook 2013 を拡張する microsoft outlook 2010 および64ビット MAPI の導入により、完全な実装には従来の32ビット API より多くのものが必要になります。 新しいプロジェクト (CodePlex web サイトに投稿された mapi スタブライブラリ) は、32ビットと64ビットの両方の mapi アプリケーションのビルドをサポートする Mapi32 のためのドロップイン置換を提供します。 MAPIStubLibrary を使用すると、MAPI を明示的にリンクする必要がなくなり、これを構築する必要があります。リンカー設定から Mapi32 を削除して、MAPIStubLibrary に置き換えることができます。コードをこれ以上変更する必要はありません。 また、このライブラリファイルに含まれている新しいエクスポートを処理するために、 **LoadLibrary**、 **GetProcAddress**、および**FreeLibrary**コードを記述する必要がなくなります。これは、明示的なリンクを使用した場合に必要になります。 
  
このライブラリからリンクされているいくつかの新機能には、次のようなものがあります。 Mapi32 では使用できません。
  
- [GetDefCachedMode](getdefcachedmode.md)    
- [HrGetGALFromEmsmdbUID](hrgetgalfromemsmdbuid.md)   
- [HrOpenOfflineObj](hropenofflineobj.md)    
- [MAPICrashRecovery](mapicrashrecovery.md)   
- [OpenStreamOnFileW](openstreamonfilew.md)    
- [WrapCompressedRTFStreamEx](wrapcompressedrtfstreamex.md)
    
mapi スタブライブラリを組み込む別の方法として、ソースファイル MapiStubLibrary と StubUtils を直接プロジェクトにコピーして、Mapi32 へのリンケージを削除し、mapi に明示的にリンクされたコードを削除することができます。
  
mapi スタブライブラリファイルにアクセスし、それをプロジェクトに構築して統合する方法、および使用する状況や理由など、このライブラリに関する質問については、CodePlex サイトの[mapi スタブライブラリ](https://mapistublibrary.codeplex.com/documentation)を参照してください。 
  
## <a name="see-also"></a>関連項目

- [MAPI プログラミングの概要](mapi-programming-overview.md)
- [MAPI サブシステムのインストール](installing-the-mapi-subsystem.md)
- [MAPI ヘッダーファイルをインストールする](how-to-install-mapi-header-files.md)
- [読み込む MAPI の特定のバージョンを選択する](how-to-choose-a-specific-version-of-mapi-to-load.md)
- [どのリンク方法を使用するかを決定する](https://msdn.microsoft.com/library/253b8k2c.aspx)
- [実行可能ファイルを DLL にリンクする](https://msdn.microsoft.com/library/9yd93633.aspx)
- [MAPI DLL の MSI キーを設定する](https://msdn.microsoft.com/library/ee909494%28v=VS.85%29.aspx)

