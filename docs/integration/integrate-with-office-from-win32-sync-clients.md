---
title: Win32 同期クライアントからの Office との統合
manager: soliver
ms.date: 07/29/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 348555d3-3cd4-4e4a-b5ad-436571c25251
description: サード パーティ製 Win32 同期クライアントを Excel Mobile、 PowerPoint Mobile、および Word MobileOffice アプリケーションと統合します。
ms.openlocfilehash: 83bc6e4cddc17e539b371999fff620c72c595534
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303137"
---
# <a name="integrate-with-office-from-win32-sync-clients"></a>Win32 同期クライアントからの Office との統合

サード パーティ製 Win32 同期クライアントを Excel Mobile、 PowerPoint Mobile、および Word MobileOffice アプリケーションと統合します。 
  
同期ルート プロバイダーとして登録することにより、Windows ユニバーサル アプリを Excel Mobile、PowerPoint Mobile、および Word Mobile クライアントと統合できます。 この記事では、Win32 同期クライアントが Office アプリケーションと共に適切に動作するようにするため、適用できるベスト プラクティスについて説明します。
  
この統合では、Win32 同期クライアントに同期エンジンがあることが必要です。
  
## <a name="register-as-a-sync-root-provider"></a>同期ルート プロバイダーとして登録する

同期クライアントが同期ルート プロバイダーとして登録されていない限り、Office は同期フォルダー内のファイルを通常のローカル ファイルと同様の方法で扱います。つまり、ユーザーがドキュメントを共有しようとすると、Office は「OneDrive に移動する」オプションを示します。同期するファイルでこれを回避するには、同期ルート プロバイダーとして登録する必要があります。登録する方法について詳しくは、「[クラウド ストレージ プロバイダーの統合](https://msdn.microsoft.com/library/windows/desktop/dn889934%28v=vs.85%29.aspx)」を参照してください。
  
## <a name="integrate-your-app-into-the-root-node-of-the-navigation-pane"></a>アプリをナビゲーション ウィンドウのルート ノードに統合する

Win32 同期クライアントがファイル エクスプ ローラーと Windows ファイル ピッカーでルート ノードとして表示されるようにするには、アプリをルート レベルに統合する必要があります。これを行う方法については、「[クラウド ストレージ プロバイダーの統合](https://msdn.microsoft.com/library/windows/desktop/dn889934%28v=vs.85%29.aspx)」を参照してください。 
  
## <a name="add-your-sync-folder-as-a-document-library-optional"></a>同期フォルダーをドキュメント ライブラリとして追加する (省略可能)

Office で、ユーザーは単一の操作でドキュメント ライブラリにドキュメントを作成できます。ドキュメント ライブラリに同期場所に追加するには、[SHAddFolderPathToLibrary 関数](https://msdn.microsoft.com/library/windows/desktop/dd378432%28v=vs.85%29.aspx)を使用します。 
  
## <a name="see-also"></a>関連項目
<a name="bk_addresources"> </a>

- [Office との統合](integrate-with-office.md)
    
- [Windows ユニバーサル アプリからの Office との統合](integrate-with-office-from-windows-universal-apps.md)
    

