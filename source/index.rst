Facebook Templates API
======================

This document introduces and explains the use of Facebook Templates API for previewing campaign images on the ICN platform.

Introduction
^^^^^^^^^^^^

Facebook Templates API for `ICN <http://icrowdnewswire.com>`_ provides an endpoint to preview a Facebook campaign image. Let's see how we can consume the endpoint.


API Endpoints
^^^^^^^^^^^^^

.. http:post:: /

    Preview a Facebook campaign image.

    Example Request
        .. sourcecode:: http

            POST / HTTP/1.1
            Host: icrowdnewswire.com/api/templates/
            User-Agent: curl/7.65.3
            Accept: */*

    :reqheader Content-Type: application/x-www-form-urlencoded
    :form heading: Heading for the overlay.
    :form description: Description for the overlay.
    :form image: ``[Binary] Image`` to put overlay on.
    :form no_top: Whether the overlay should skip positioning the overlay from the top.
    :form bottom: Bottom position of the overlay in pixels.
    :form bg_color: Background color of the overlay.
    :form opacity: Opacity of the overlay.

    Example Response
        .. image:: _static/images/bottom-left.png


    :form heading: Michael Jackson
    :form descripton: Dangerous Tour Live - 1992
    :form image: ``Binary``
    :form no_top: ``1``
    :form bottom: ``20``
    :form bg_color: ``Indigo``
    :form opacity: ``0.6``

    .. note::
        The response is returned as an HTML document.


Possible Parameters
###################

Below are the form parameters you can pass to customize the overlay.:

    * **heading** - Heading of the overlay. ``Required``
    * **image** - Image to be used for preview. Must be in binary. ``Required``
    * **description** - Description of the overlay.
    * **top** - Top position of the overlay in pixels.
    * **left** - Left position of the overlay in pixels.
    * **bottom** - Bottom position of the overlay in pixels.
    * **right** - Right position of the overlay in pixels.
    * **padding_left** - Left padding of the overlay in pixels.
    * **padding_right** - Right padding of the overlay in pixels.
    * **no_left** - Non null value indicating if the overlay should skip rendering from left.
    * **no_right** - Non null value indicating if the overlay should skip rendering from right.
    * **bg_color** - Background color of the overlay.
    * **text_color** - Text color of the overlay.
    * **font_family** - Font Family to use when rendering text on the overlay. Defaults to Arial and fallbacks to Serif.
    * **opacity** - Opacity of the overlay. Possible values: ``0.1`` - ``1``


.. toctree::
   :maxdepth: 2

