---
title: Win32 同期クライアントからの Office との統合
manager: soliver
ms.date: 07/29/2015
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 348555d3-3cd4-4e4a-b5ad-436571c25251
description: サード パーティ製 Win32 同期クライアントを Excel Mobile、 PowerPoint Mobile、および Word MobileOffice アプリケーションと統合します。
ms.openlocfilehash: ad0c93bb03ba3b23c8395853bec77b8dec29a333
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59557338"
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
    

