---
title: JavaScript ライブラリと REST リファレンス (Project Server)
manager: soliver
ms.date: 08/10/2016
ms.audience: Developer
localization_priority: Normal
ms.assetid: 67b47b8b-d34b-4fad-af49-0c258c345ad2
description: Project Server 2013 の JavaScript ライブラリと REST リファレンスには、JavaScript オブジェクト モデルと、Project Server の機能にアクセスするために使用する REST インターフェイスに関する情報が含まれている。 これらの API を使用して、Project Server 2013 および Project Online にアクセスするクロスブラウザー Web アプリ、Project Professional 2013 アドイン、および Windows 以外のデバイス用のアプリを開発できます。
ms.openlocfilehash: fb58de1e3858a39f42cc9a643a7394cec191a462
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32358108"
---
# <a name="javascript-library-and-rest-reference-for-project-server"></a>JavaScript ライブラリと REST リファレンス (Project Server)

Project Server 2013 の JavaScript ライブラリと REST リファレンスには、JavaScript オブジェクト モデルと、Project Server の機能にアクセスするために使用する REST インターフェイスに関する情報が含まれている。 これらの API を使用して、Project Server 2013 および Project Online にアクセスするクロスブラウザー Web アプリ、Project Professional 2013 アドイン、および Windows 以外のデバイス用のアプリを開発できます。
  
> [!NOTE]
> JavaScript オブジェクト モデルと REST インターフェイスは、Project クライアント側オブジェクト モデル (CSOM) に合わせて配置されます。 これらは、CSOM の **Microsoft.ProjectServer.Client** 名前空間と同等の機能を提供します。 
  
ファイル内の PS Projectで定義されている JavaScript オブジェクト モデルを使用して、サーバー[](https://msdn.microsoft.com/library/e3156167-a4fd-1bf6-8d1c-e180de1844ed%28Office.15%29.aspx)の機能にアクセス `%ProgramFiles%\Common Files\Microsoft Shared\Web Server Extensions\15\TEMPLATE\LAYOUTS\PS.js` できます。 [PS](https://msdn.microsoft.com/library/e3156167-a4fd-1bf6-8d1c-e180de1844ed%28Office.15%29.aspx) [名前空間の ProjectContext](https://msdn.microsoft.com/library/a490b675-a845-ee94-3877-b99ada9bf2b0%28Office.15%29.aspx)オブジェクトは、JavaScript オブジェクト モデルのエントリ ポイントです。 
  
> [!NOTE]
> JavaScript オブジェクト モデルを参照し、デバッグに役立つには、同じディレクトリPS.debug.jsファイルを使用します。 リモート コンピューターでの開発を支援するために[、Project 2013 SDK](https://www.microsoft.com/en-us/download/details.aspx?id=30435)のダウンロードには、CSOM の .NET Framework アセンブリと PS.js ファイルと PS.debug.js ファイルが含まれています。 
  
REST インターフェイスを使用Projectサーバーの機能にアクセスすることもできます。 REST インターフェイスのエントリ ポイントは **ProjectServer** リソースで、エンドポイント URI を使用して  `https://ServerName/pwaName/_api/ProjectServer` アクセスします。 たとえば、次のクエリは、指定したプロジェクト内の割り当てを取得します  _(ServerName_ と  _pwaName_ を置き換え、プロジェクトに一致する GUID を変更します)。
  
`https://ServerName/pwaName/_api/ProjectServer/Projects('263fc8d7-427c-e111-92fc-00155d3ba208')/Assignments`

**ProjectServer リソースについては**[、REST インターフェイスの ProjectServer リソースで説明されています](https://msdn.microsoft.com/library/a490b675-a845-ee94-3877-b99ada9bf2b0%28Office.15%29.aspx#bk_ProjectServerResources)。 その他の REST リソースについては、このリファレンスの対応する JavaScript オブジェクトとメンバーのドキュメントで説明されています。 REST の使用の詳細については、「Project Server および SharePoint REST サービスを使用したプログラミングのクライアント側オブジェクト モデル[(CSOM)」](client-side-object-model-csom-for-project-2013.md)を[参照してください](https://msdn.microsoft.com/library/fp142385%28office.15%29.aspx)。
  
## <a name="javascript-library-and-rest-reference-for-project-server"></a>JavaScript ライブラリと REST リファレンス (Project Server)
<a name="pj15_JavaScriptAPIReference_PS"> </a>

- [PS.js JavaScript ライブラリと REST リファレンス](https://msdn.microsoft.com/library/5a140021-380a-d9e0-e36d-106df85f56d6%28Office.15%29.aspx)JavaScript オブジェクト モデルと、サーバー 2013 の REST Projectします。 
    
## <a name="see-also"></a>関連項目
<a name="bk_addresources"> </a>

- [Project 2013 開発者向けドキュメント](project-2013-developer-documentation.md)   
- [Project Server のクライアント側オブジェクト モデル (CSOM)](client-side-object-model-csom-for-project-2013.md)   
- [JavaScript オブジェクト モデルの使用を開始する](getting-started-with-the-project-server-2013-javascript-object-model.md)  
- [JavaScript オブジェクト モデルを使用してプロジェクトを操作する](create-retrieve-update-delete-projects-using-project-server-javascript.md)
    

