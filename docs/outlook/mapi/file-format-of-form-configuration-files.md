---
title: フォーム構成ファイルのファイル形式
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 86e4ebd9-6df2-4346-9ce9-580f80a83884
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: d07d88d7b8b892a82832f91989e322ea3b32e040
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415552"
---
# <a name="file-format-of-form-configuration-files"></a><span data-ttu-id="756ee-103">フォーム構成ファイルのファイル形式</span><span class="sxs-lookup"><span data-stu-id="756ee-103">File format of form configuration files</span></span>

<span data-ttu-id="756ee-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="756ee-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="756ee-105">フォーム構成ファイルは、フォームを定義するためにフォーム開発者によって作成された書式設定されたファイルです。</span><span class="sxs-lookup"><span data-stu-id="756ee-105">A form configuration file is a formatted file created by form developers to define a form.</span></span>
  
<span data-ttu-id="756ee-106">フォーム構成ファイルはフォーム管理者がフォームを読み込むため、フォーム構成ファイルを使用して各フォームを定義する必要があります。</span><span class="sxs-lookup"><span data-stu-id="756ee-106">Because form configuration files are used by form managers to load forms, each form must be defined using a form configuration file.</span></span> <span data-ttu-id="756ee-107">フォーム構成ファイルには、.cfg ファイル名の拡張子が必要です。</span><span class="sxs-lookup"><span data-stu-id="756ee-107">Form configuration files must have the .cfg filename extension.</span></span> <span data-ttu-id="756ee-108">このファイルは、初期化ファイル (Windows) の一般的.iniします。</span><span class="sxs-lookup"><span data-stu-id="756ee-108">The file follows the general syntax of a Windows initialization file (.ini file).</span></span> 

<span data-ttu-id="756ee-109">このセクションは名前付きセクションに分かれ、各セクションには一連のエントリと値が含まれます。</span><span class="sxs-lookup"><span data-stu-id="756ee-109">It is divided into named sections, and each section contains a series of entries and values.</span></span> <span data-ttu-id="756ee-110">値には、文字列、表示される文字列、プラットフォーム文字列、パス、整数、またはグローバル一意識別子 GUID のいずれかの種類 **があります**。</span><span class="sxs-lookup"><span data-stu-id="756ee-110">Values have one of the following types: string, displayed string, platform string, path, integer, or globally unique identifier, **GUID**.</span></span> <span data-ttu-id="756ee-111">フォーム構成ファイルは、テキスト ファイルを保存できる任意のテキスト エディターまたはワード プロセッサで作成できます。</span><span class="sxs-lookup"><span data-stu-id="756ee-111">Form configuration files can be created with any text editor or word processor that is capable of saving text files.</span></span>
  

