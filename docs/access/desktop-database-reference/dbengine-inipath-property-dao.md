---
title: IniPath プロパティ (DAO)
TOCTitle: IniPath Property
ms:assetid: b18cace5-4e53-d011-6373-f4ac64556fd4
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822009(v=office.15)
ms:contentKeyID: 48547151
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053070
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: f14f9f2d028bb8a9a8e71bc9d7b97ea5672466f1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294296"
---
# <a name="dbengineinipath-property-dao"></a><span data-ttu-id="c37ea-102">IniPath プロパティ (DAO)</span><span class="sxs-lookup"><span data-stu-id="c37ea-102">DBEngine.IniPath property (DAO)</span></span>


<span data-ttu-id="c37ea-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="c37ea-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="c37ea-104">Microsoft Access データベース エンジン用の値が含まれた Windows レジストリ キーに関する情報を設定または取得します (Microsoft Access ワークスペースのみ)。</span><span class="sxs-lookup"><span data-stu-id="c37ea-104">Sets or returns information about the Windows Registry key that contains values for the Microsoft Access database engine (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="c37ea-105">構文</span><span class="sxs-lookup"><span data-stu-id="c37ea-105">Syntax</span></span>

<span data-ttu-id="c37ea-106">*式*。IniPath</span><span class="sxs-lookup"><span data-stu-id="c37ea-106">*expression* .IniPath</span></span>

<span data-ttu-id="c37ea-107">\*式\***DBEngine**オブジェクトを表す変数を取得します。</span><span class="sxs-lookup"><span data-stu-id="c37ea-107">*expression* A variable that represents a **DBEngine** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="c37ea-108">注釈</span><span class="sxs-lookup"><span data-stu-id="c37ea-108">Remarks</span></span>

<span data-ttu-id="c37ea-109">Windows レジストリを使用して、Microsoft access データベースエンジンを構成できます。</span><span class="sxs-lookup"><span data-stu-id="c37ea-109">You can configure the Microsoft Access database engine with the Windows Registry.</span></span> <span data-ttu-id="c37ea-110">このレジストリを使用すると、インストール可能な ISAM DLL などのオプションを設定できます。</span><span class="sxs-lookup"><span data-stu-id="c37ea-110">You can use the Registry to set options, such as installable ISAM DLLs.</span></span>

<span data-ttu-id="c37ea-p102">このオプションを有効にするには、 **IniPath** プロパティを設定してから、アプリケーションで他の DAO コードを呼び出す必要があります。この設定の有効範囲は使用するアプリケーションに限定され、範囲を変更するにはアプリケーションを再起動する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c37ea-p102">For this option to have any effect, you must set the **IniPath** property before your application invokes any other DAO code. The scope of this setting is limited to your application and can't be changed without restarting your application.</span></span>

<span data-ttu-id="c37ea-p103">また、レジストリを使用すると、インストール可能な ISAM データベース ドライバーの初期化パラメーターを用意できます。たとえば、Paradox バージョン 4.0 を使用するには、 **IniPath** プロパティを、該当するパラメーターが含まれたレジストリの一部の値に設定します。</span><span class="sxs-lookup"><span data-stu-id="c37ea-p103">You also use the Registry to provide initialization parameters for some installable ISAM database drivers. For example, to use Paradox version 4.0, set the **IniPath** property to a part of the Registry containing the appropriate parameters.</span></span>

<span data-ttu-id="c37ea-115">このプロパティは、hkey\_ローカル\_コンピューターまたは\_hkey\_ローカルユーザーのいずれかを認識します。</span><span class="sxs-lookup"><span data-stu-id="c37ea-115">This property recognizes either HKEY\_LOCAL\_MACHINE or HKEY\_LOCAL\_USER.</span></span> <span data-ttu-id="c37ea-116">ルートキーが指定されていない場合、\_既定\_値は HKEY ローカルコンピューターになります。</span><span class="sxs-lookup"><span data-stu-id="c37ea-116">If no root key is supplied, the default is HKEY\_LOCAL\_MACHINE.</span></span>

