---
title: JavaScript ライブラリとプロジェクトのサーバーの残りの部分参照
manager: soliver
ms.date: 08/10/2016
ms.audience: Developer
localization_priority: Normal
ms.assetid: 67b47b8b-d34b-4fad-af49-0c258c345ad2
description: JavaScript ライブラリと残りの部分参照は、Project Server 2013 には、JavaScript オブジェクト モデルおよび Project Server の機能にアクセスするために使用する REST インターフェイスに関する情報が含まれています。 これらの Api を使用すると、ブラウザー間の web アプリケーション、プロジェクトの評価のためのアドインの場合、および Project Server 2013 とオンラインのプロジェクトにアクセスする Windows 以外のデバイス用のアプリケーションを開発します。
ms.openlocfilehash: fb58de1e3858a39f42cc9a643a7394cec191a462
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25399033"
---
# <a name="javascript-library-and-rest-reference-for-project-server"></a>JavaScript ライブラリとプロジェクトのサーバーの残りの部分参照

JavaScript ライブラリと残りの部分参照は、Project Server 2013 には、JavaScript オブジェクト モデルおよび Project Server の機能にアクセスするために使用する REST インターフェイスに関する情報が含まれています。 これらの Api を使用すると、ブラウザー間の web アプリケーション、プロジェクトの評価のためのアドインの場合、および Project Server 2013 とオンラインのプロジェクトにアクセスする Windows 以外のデバイス用のアプリケーションを開発します。
  
> [!NOTE]
> JavaScript オブジェクト モデルと REST インターフェイスは、Project Server のクライアント側オブジェクト モデル (CSOM) に沿って配置します。 CSOM で**Microsoft.ProjectServer.Client**の名前空間と同等の機能を提供します。 
  
Project Server の機能をアクセスするには、JavaScript オブジェクト モデルを通じて、 [PS](https://msdn.microsoft.com/library/e3156167-a4fd-1bf6-8d1c-e180de1844ed%28Office.15%29.aspx)の名前空間で定義されている、`%ProgramFiles%\Common Files\Microsoft Shared\Web Server Extensions\15\TEMPLATE\LAYOUTS\PS.js`ファイルです。 [PS](https://msdn.microsoft.com/library/e3156167-a4fd-1bf6-8d1c-e180de1844ed%28Office.15%29.aspx)名前空間内の[ProjectContext](https://msdn.microsoft.com/library/a490b675-a845-ee94-3877-b99ada9bf2b0%28Office.15%29.aspx)オブジェクトは、JavaScript オブジェクト モデルへのエントリ ポイントです。 
  
> [!NOTE]
> JavaScript オブジェクト モデルを参照して、デバッグに役立つように、同じディレクトリに PS.debug.js ファイルを使用できます。 [Project 2013 SDK のダウンロード](https://www.microsoft.com/en-us/download/details.aspx?id=30435)ではリモート コンピューター上の開発を支援するため、CSOM および PS.js と PS.debug.js ファイルの.NET Framework アセンブリが含まれます。 
  
REST インターフェイスで Project Server の機能をアクセスすることもできます。 REST インターフェイスへのエントリ ポイントでは、 **ProjectServer**リソースを使用してアクセスすることが、`https://ServerName/pwaName/_api/ProjectServer`エンドポイントの URI です。 次のクエリが指定されたプロジェクト内の割り当てを取得するなど、(_サーバー名_と_pwaName_を交換し、プロジェクトに一致する GUID を変更) します。
  
`https://ServerName/pwaName/_api/ProjectServer/Projects('263fc8d7-427c-e111-92fc-00155d3ba208')/Assignments`

**ProjectServer**リソースには、 [REST インターフェイスでは、ProjectServer リソース](https://msdn.microsoft.com/library/a490b675-a845-ee94-3877-b99ada9bf2b0%28Office.15%29.aspx#bk_ProjectServerResources)が記載されています。 他の REST リソースは、対応する JavaScript オブジェクトとメンバーでは、この参照のマニュアルで説明します。 残りの部分の使用に関する詳細については、 [Project Server のクライアント側オブジェクト モデル (CSOM)](client-side-object-model-csom-for-project-2013.md)と[SharePoint 2013 の REST サービスを使用してプログラミング](https://msdn.microsoft.com/library/fp142385%28office.15%29.aspx)を参照してください。
  
## <a name="javascript-library-and-rest-reference-for-project-server"></a>JavaScript ライブラリとプロジェクトのサーバーの残りの部分参照
<a name="pj15_JavaScriptAPIReference_PS"> </a>

- [PS.js JavaScript ライブラリおよび他の参照](https://msdn.microsoft.com/library/5a140021-380a-d9e0-e36d-106df85f56d6%28Office.15%29.aspx)Project Server 2013 の JavaScript オブジェクト モデルと REST インターフェイスに関する情報が含まれています。 
    
## <a name="see-also"></a>関連項目
<a name="bk_addresources"> </a>

- [Project 2013 開発者向けドキュメント](project-2013-developer-documentation.md)   
- [Project Server のクライアント側オブジェクト モデル (CSOM)](client-side-object-model-csom-for-project-2013.md)   
- [JavaScript オブジェクト モデルの作業の開始](getting-started-with-the-project-server-2013-javascript-object-model.md)  
- [JavaScript オブジェクト モデルを使用してプロジェクトを操作する](create-retrieve-update-delete-projects-using-project-server-javascript.md)
    

