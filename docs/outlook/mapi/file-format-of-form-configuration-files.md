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
# <a name="file-format-of-form-configuration-files"></a><span data-ttu-id="4cf49-103">フォーム構成ファイルのファイル形式</span><span class="sxs-lookup"><span data-stu-id="4cf49-103">File format of form configuration files</span></span>

<span data-ttu-id="4cf49-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4cf49-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4cf49-105">フォーム構成ファイルは、フォーム開発者がフォームを定義するために作成した形式のファイルです。</span><span class="sxs-lookup"><span data-stu-id="4cf49-105">A form configuration file is a formatted file created by form developers to define a form.</span></span>
  
<span data-ttu-id="4cf49-106">フォーム構成ファイルはフォームマネージャーによってフォームの読み込みに使用されるため、フォーム構成ファイルを使用して各フォームを定義する必要があります。</span><span class="sxs-lookup"><span data-stu-id="4cf49-106">Because form configuration files are used by form managers to load forms, each form must be defined using a form configuration file.</span></span> <span data-ttu-id="4cf49-107">フォーム構成ファイルには、拡張子が cfg である必要があります。</span><span class="sxs-lookup"><span data-stu-id="4cf49-107">Form configuration files must have the .cfg filename extension.</span></span> <span data-ttu-id="4cf49-108">このファイルは、Windows 初期化ファイル (.ini ファイル) の一般的な構文に従います。</span><span class="sxs-lookup"><span data-stu-id="4cf49-108">The file follows the general syntax of a Windows initialization file (.ini file).</span></span> 

<span data-ttu-id="4cf49-109">このセクションは、指定されたセクションに分かれており、各セクションには一連のエントリと値が含まれています。</span><span class="sxs-lookup"><span data-stu-id="4cf49-109">It is divided into named sections, and each section contains a series of entries and values.</span></span> <span data-ttu-id="4cf49-110">値の型は、string、表示された文字列、プラットフォーム文字列、パス、整数、またはグローバル一意識別子 ( **GUID**) のいずれかです。</span><span class="sxs-lookup"><span data-stu-id="4cf49-110">Values have one of the following types: string, displayed string, platform string, path, integer, or globally unique identifier, **GUID**.</span></span> <span data-ttu-id="4cf49-111">フォーム構成ファイルは、テキストファイルの保存が可能なテキストエディターまたはワープロを使用して作成できます。</span><span class="sxs-lookup"><span data-stu-id="4cf49-111">Form configuration files can be created with any text editor or word processor that is capable of saving text files.</span></span>
  

