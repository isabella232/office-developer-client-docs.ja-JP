---
title: Outlook PIA のインストールと参照
TOCTitle: Installing and referencing the Outlook PIA
ms:assetid: b1afd047-dcbb-480f-ba74-993d7d7114cb
ms:mtpsurl: https://msdn.microsoft.com/library/office/bb646840(v=office.15)
ms:contentKeyID: 55119774
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: 42e79fcd6cf9575f43722d7ba467b028ef6c3e16
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25405512"
---
# <a name="installing-and-referencing-the-outlook-pia"></a><span data-ttu-id="27b98-102">Outlook PIA のインストールと参照</span><span class="sxs-lookup"><span data-stu-id="27b98-102">Installing and Referencing the Outlook PIA</span></span>

<span data-ttu-id="27b98-103">Outlook 管理アドインで PIA の情報を取り込むには、その前にグローバル アセンブリ キャッシュ (GAC) に Outlook プライマリ相互運用機能アセンブリ (PIA) をインストールしておく必要があります。</span><span class="sxs-lookup"><span data-stu-id="27b98-103">You must have the Outlook Primary Interop Assembly (PIA) installed in the Global Assembly Cache (GAC) before you can incorporate information from the PIA in an Outlook managed add-in.</span></span> <span data-ttu-id="27b98-104">既定では、PIA は開発コンピューターに Office をインストールするときに自動的にインストールされます。</span><span class="sxs-lookup"><span data-stu-id="27b98-104">By default, the PIA is installed automatically when you install Office on the development computer.</span></span> <span data-ttu-id="27b98-105">ただし、PIA を別途インストールする必要がある場合は、「[Office ソリューションを開発できるようにコンピューターを構成する](https://docs.microsoft.com/visualstudio/vsto/configuring-a-computer-to-develop-office-solutions?view=vs-2017)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="27b98-105">However, if you need to install the PIA separately, see [Configure a computer to develop Office solutions](https://docs.microsoft.com/visualstudio/vsto/configuring-a-computer-to-develop-office-solutions?view=vs-2017).</span></span>


> [!NOTE] 
> <span data-ttu-id="27b98-106">Office PIA をインストールするには開発コンピューターで管理者でなければなりません。</span><span class="sxs-lookup"><span data-stu-id="27b98-106">You must be an administrator on the development computer to install the Office PIAs.</span></span>

<span data-ttu-id="27b98-p102">インストール後、Visual Studio を使用して管理オブジェクトを作成している場合、[ Microsoft Outlook 15.0 Object Library] コンポーネントへの参照を追加できます。その後、オブジェクト ブラウザーの [ **Microsoft.Office.Interop.Outlook**] 名前空間の下に、Outlook オブジェクト モデル内のオブジェクトに対応する名前の、PIA 内の管理インターフェイスが表示されます。</span><span class="sxs-lookup"><span data-stu-id="27b98-p102">After installation, if you are using Visual Studio to create the managed project, you can add a reference to the Microsoft Outlook 15.0 Object Library component. Subsequently, in the object browser, under the **Microsoft.Office.Interop.Outlook** namespace, you can see managed interfaces in the PIA that have names corresponding to objects in the Outlook object model.</span></span>

## <a name="see-also"></a><span data-ttu-id="27b98-109">関連項目</span><span class="sxs-lookup"><span data-stu-id="27b98-109">See also</span></span>

- [<span data-ttu-id="27b98-110">Office プライマリ相互運用機能アセンブリのインストール</span><span class="sxs-lookup"><span data-stu-id="27b98-110">Install Office primary interop assemblies</span></span>](https://docs.microsoft.com/visualstudio/vsto/how-to-install-office-primary-interop-assemblies?view=vs-2017)
- [<span data-ttu-id="27b98-111">Outlook PIA のアーキテクチャ</span><span class="sxs-lookup"><span data-stu-id="27b98-111">Architecture of the Outlook PIA</span></span>](architecture-of-the-outlook-pia.md)

