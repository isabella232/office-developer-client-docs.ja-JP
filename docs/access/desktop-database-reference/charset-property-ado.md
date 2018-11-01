---
title: Charset プロパティ (ADO)
TOCTitle: Charset property (ADO)
ms:assetid: 454f664e-6d62-eec9-487d-882c2f9503b0
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249213(v=office.15)
ms:contentKeyID: 48544551
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 46d9016e84b507526fa36202169f532e9ee7d738
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25887790"
---
# <a name="charset-property-ado"></a><span data-ttu-id="9ff4e-102">Charset プロパティ (ADO)</span><span class="sxs-lookup"><span data-stu-id="9ff4e-102">Charset property (ADO)</span></span>


<span data-ttu-id="9ff4e-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="9ff4e-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="9ff4e-104">テキスト [Stream](stream-object-ado.md) の内容を変換して Stream オブジェクト内部バッファーに格納するための文字セットを示します。</span><span class="sxs-lookup"><span data-stu-id="9ff4e-104">Indicates the character set into which the contents of a text [Stream](stream-object-ado.md) should be translated for storage in the Stream objects internal buffer.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="9ff4e-105">設定値および戻り値</span><span class="sxs-lookup"><span data-stu-id="9ff4e-105">Settings and return values</span></span>

<span data-ttu-id="9ff4e-106">**Stream** の内容の変換に使用される文字セットを指定する文字列型 ( **String** ) の値を設定または取得します。</span><span class="sxs-lookup"><span data-stu-id="9ff4e-106">Sets or returns a **String** value that specifies the character set into which the contents of the **Stream** will be translated.</span></span> <span data-ttu-id="9ff4e-107">既定値は "Unicode" です。</span><span class="sxs-lookup"><span data-stu-id="9ff4e-107">The default value is "Unicode".</span></span> <span data-ttu-id="9ff4e-108">指定可能な値は、インターフェイスを介してインターネット文字セット文字列として渡すことのできる通常の文字列 ("iso-8859-1"、"Windows-1252" など) です。</span><span class="sxs-lookup"><span data-stu-id="9ff4e-108">Allowed values are typical strings passed over the interface as Internet character set strings (for example, "iso-8859-1", "Windows-1252", etc.).</span></span> <span data-ttu-id="9ff4e-109">システムで認識されている文字セットの文字列のリスト、HKEY のサブキーを参照してください\_クラス\_ルート\\MIME\\データベース\\Windows レジストリ内の文字セットです。</span><span class="sxs-lookup"><span data-stu-id="9ff4e-109">For a list of the character set strings that is known by a system, see the subkeys of HKEY\_CLASSES\_ROOT\\MIME\\Database\\Charset in the Windows Registry.</span></span>

## <a name="remarks"></a><span data-ttu-id="9ff4e-110">解説</span><span class="sxs-lookup"><span data-stu-id="9ff4e-110">Remarks</span></span>

<span data-ttu-id="9ff4e-p102">テキスト **Stream** オブジェクトでは、 **Charset** プロパティで指定された文字セットでテキスト データが格納されます。既定値は Unicode です。 **Charset** プロパティは、 **Stream** に送るデータの変換、または **Stream** から受け取るデータの変換に使用されます。たとえば、 **Stream** に ISO-8859-1 データが格納されており、そのデータが BSTR にコピーされる場合、 **Stream** オブジェクトはデータを Unicode に変換します。逆の変換も同じように行われます。</span><span class="sxs-lookup"><span data-stu-id="9ff4e-p102">In a text **Stream** object, text data is stored in the character set specified by the **Charset** property. The default is Unicode. The **Charset** property is used for converting data going into the **Stream** or coming out of the **Stream**. For example, if the **Stream** contains ISO-8859-1 data and that data is copied to a BSTR, the **Stream** object will convert the data to Unicode. The reverse is also true.</span></span>

<span data-ttu-id="9ff4e-116">開いている **Stream** の場合、 [Charset](position-property-ado.md) を設定するには、現在の **Position** が **Stream** の先頭 (0) になっている必要があります。</span><span class="sxs-lookup"><span data-stu-id="9ff4e-116">For an open **Stream**, the current [Position](position-property-ado.md) must be at the beginning of the **Stream** (0) to be able to set **Charset**.</span></span>

<span data-ttu-id="9ff4e-p103">**Charset** は、テキスト **Stream** オブジェクト ([Type](type-property-ado-stream.md) が **adTypeText**) でのみ使用されます。**Type** が **adTypeBinary** の場合、このプロパティは無視されます。</span><span class="sxs-lookup"><span data-stu-id="9ff4e-p103">**Charset** is used only with text **Stream** objects ([Type](type-property-ado-stream.md) is **adTypeText**). This property is ignored if **Type** is **adTypeBinary**.</span></span>

