---
title: Project Server の JavaScript ライブラリと REST リファレンス
manager: soliver
ms.date: 08/10/2016
ms.audience: Developer
localization_priority: Normal
ms.assetid: 67b47b8b-d34b-4fad-af49-0c258c345ad2
description: 「project server 2013 の javascript ライブラリと rest リファレンス」には、javascript オブジェクトモデル、および project server 機能へのアクセスに使用する rest インターフェイスに関する情報が記載されています。 これらの api を使用して、ブラウザー間の web アプリ、project Professional 2013 アドイン、および project Server 2013 および project Online にアクセスする Windows 以外のデバイス用アプリを開発できます。
ms.openlocfilehash: fb58de1e3858a39f42cc9a643a7394cec191a462
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32358108"
---
# <a name="javascript-library-and-rest-reference-for-project-server"></a>Project Server の JavaScript ライブラリと REST リファレンス

「project server 2013 の javascript ライブラリと rest リファレンス」には、javascript オブジェクトモデル、および project server 機能へのアクセスに使用する rest インターフェイスに関する情報が記載されています。 これらの api を使用して、ブラウザー間の web アプリ、project Professional 2013 アドイン、および project Server 2013 および project Online にアクセスする Windows 以外のデバイス用アプリを開発できます。
  
> [!NOTE]
> JavaScript オブジェクトモデルと REST インターフェイスは、Project Server クライアント側オブジェクトモデル (csom) と連携します。 これらは csom の**microsoft.projectserver.client**名前空間に相当する機能を提供します。 
  
ファイル内の PS 名前空間で定義されている JavaScript オブジェクトモデルを使用して、Project Server の機能にアクセスできます。 [](https://msdn.microsoft.com/library/e3156167-a4fd-1bf6-8d1c-e180de1844ed%28Office.15%29.aspx) `%ProgramFiles%\Common Files\Microsoft Shared\Web Server Extensions\15\TEMPLATE\LAYOUTS\PS.js` [PS](https://msdn.microsoft.com/library/e3156167-a4fd-1bf6-8d1c-e180de1844ed%28Office.15%29.aspx)名前空間の[projectcontext](https://msdn.microsoft.com/library/a490b675-a845-ee94-3877-b99ada9bf2b0%28Office.15%29.aspx)オブジェクトは、JavaScript オブジェクトモデルへのエントリポイントです。 
  
> [!NOTE]
> JavaScript オブジェクトモデルを参照し、デバッグに役立てるために、同じディレクトリにある .ps ファイルを使用できます。 リモートコンピューターでの開発を支援するために、 [Project 2013 SDK のダウンロード](https://www.microsoft.com/en-us/download/details.aspx?id=30435)には、csom 用の .net Framework アセンブリと、.ps および .ps ファイルが含まれています。 
  
REST インターフェイスを使用して、Project Server の機能にアクセスすることもできます。 REST インターフェイスへのエントリポイントは、 `https://ServerName/pwaName/_api/ProjectServer`エンドポイント URI を使用してアクセスする**microsoft.projectserver.client**リソースです。 たとえば、次のクエリは、指定されたプロジェクトの割り当てを取得します ( _ServerName_と_pwaName_を置き換え、GUID をプロジェクトと一致するように変更します)。
  
`https://ServerName/pwaName/_api/ProjectServer/Projects('263fc8d7-427c-e111-92fc-00155d3ba208')/Assignments`

**microsoft.projectserver.client**リソースについては、 [REST インターフェイスの「microsoft.projectserver.client resources](https://msdn.microsoft.com/library/a490b675-a845-ee94-3877-b99ada9bf2b0%28Office.15%29.aspx#bk_ProjectServerResources)」を参照してください。 その他の REST リソースについては、このリファレンスの対応する JavaScript オブジェクトおよびメンバーのドキュメントで説明されています。 REST の使用の詳細については、「 [Project Server のクライアント側オブジェクトモデル (csom)](client-side-object-model-csom-for-project-2013.md) 」および「 [SharePoint 2013 REST サービスを使用したプログラミング](https://msdn.microsoft.com/library/fp142385%28office.15%29.aspx)」を参照してください。
  
## <a name="javascript-library-and-rest-reference-for-project-server"></a>Project Server の JavaScript ライブラリと REST リファレンス
<a name="pj15_JavaScriptAPIReference_PS"> </a>

- [js JavaScript ライブラリと REST リファレンス](https://msdn.microsoft.com/library/5a140021-380a-d9e0-e36d-106df85f56d6%28Office.15%29.aspx)Project Server 2013 の JavaScript オブジェクトモデルおよび REST インターフェイスに関する情報が含まれています。 
    
## <a name="see-also"></a>関連項目
<a name="bk_addresources"> </a>

- [Project 2013 開発者向けドキュメント](project-2013-developer-documentation.md)   
- [Project Server のクライアント側オブジェクト モデル (CSOM)](client-side-object-model-csom-for-project-2013.md)   
- [JavaScript オブジェクトモデルの概要](getting-started-with-the-project-server-2013-javascript-object-model.md)  
- [JavaScript オブジェクト モデルを使用してプロジェクトを操作する](create-retrieve-update-delete-projects-using-project-server-javascript.md)
    

