---
title: Parse 関数 (Access カスタム web アプリ)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 09dee0ae-89b2-449c-a3c8-d6b270710b64
description: アプリケーションのカルチャを使用して、テキスト値を解析し、その値を特定の型で戻します。
ms.openlocfilehash: d664985ab1d7a7d33b99c52d5bab4aa714767e40
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411135"
---
# <a name="parse-function-access-custom-web-app"></a><span data-ttu-id="fa2b7-103">Parse 関数 (Access カスタム web アプリ)</span><span class="sxs-lookup"><span data-stu-id="fa2b7-103">Parse Function (Access custom web app)</span></span>

<span data-ttu-id="fa2b7-104">アプリケーションのカルチャを使用して、テキスト値を解析し、その値を特定の型で戻します。</span><span class="sxs-lookup"><span data-stu-id="fa2b7-104">Parses a text value and returns its value in a given type using the culture of the application.</span></span>
  
> [!NOTE]
> <span data-ttu-id="fa2b7-p101">この記事で説明されているクラウド ストレージ機能は、Office 2013 および Office 2016 ではサポートされなくなっているため、次のエラーが発生する可能性があります。 >  *申し訳ございません。サーバーで問題が発生しているため、現在 \<サービス\> を追加できません。後でもう一度お試しください。* > Office Online、Office for iOS、Office for Android のクラウド ストレージについて、[Office クラウド ストレージ パートナー プログラム](https://dev.office.com/programs/officecloudstorage)でお調べいただけます。</span><span class="sxs-lookup"><span data-stu-id="fa2b7-p101">The cloud storage feature described in this article is no longer supported in Office 2013 and Office 2016 and may result in the following error: >  *Sorry, we're having server problems, so we can't add \<service\> right now. Please try again later.* > For cloud storage for Office Online, Office for iOS, and Office for Android, you can look into our [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage).</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="fa2b7-107">構文</span><span class="sxs-lookup"><span data-stu-id="fa2b7-107">Syntax</span></span>

 <span data-ttu-id="fa2b7-108">**Parse**(*textexpression*、 *DataType*)</span><span class="sxs-lookup"><span data-stu-id="fa2b7-108">**Parse** (*TextExpression*, *DataType*)</span></span> 
  
<span data-ttu-id="fa2b7-109">**Parse** 関数には、以下の引数があります。</span><span class="sxs-lookup"><span data-stu-id="fa2b7-109">The **Parse** function contains the following arguments.</span></span> 
  
|<span data-ttu-id="fa2b7-110">**引数名**</span><span class="sxs-lookup"><span data-stu-id="fa2b7-110">**Argument name**</span></span>|<span data-ttu-id="fa2b7-111">**説明**</span><span class="sxs-lookup"><span data-stu-id="fa2b7-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="fa2b7-112">*TextExpression*</span><span class="sxs-lookup"><span data-stu-id="fa2b7-112">*TextExpression*</span></span>  <br/> |<span data-ttu-id="fa2b7-113">指定したデータ型になっているか解析される対象の、書式設定された値を表すテキスト式。</span><span class="sxs-lookup"><span data-stu-id="fa2b7-113">A text expression representing the formatted value to parse into the specified data type.</span></span>  <br/> |
| <span data-ttu-id="fa2b7-114">*DataType*</span><span class="sxs-lookup"><span data-stu-id="fa2b7-114">*DataType*</span></span>  <br/> |<span data-ttu-id="fa2b7-115">結果として要求されるデータ型を表すリテラル値。</span><span class="sxs-lookup"><span data-stu-id="fa2b7-115">Literal value representing the data type requested for the result.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="fa2b7-116">注釈</span><span class="sxs-lookup"><span data-stu-id="fa2b7-116">Remarks</span></span>

<span data-ttu-id="fa2b7-p102">**Parse** は、文字列から日付/時刻または数値に型を変換する場合にのみ使用します。一般的な型変換では、 **Convert** 関数を使用します。文字列値の解析には、一定のパフォーマンス オーバーヘッドが発生することに注意してください。</span><span class="sxs-lookup"><span data-stu-id="fa2b7-p102">Use **Parse** only for converting from string to date/time and number types. For general type conversions, use the **Convert** function. Keep in mind that there is a certain performance overhead in parsing the string value.</span></span> 
  

