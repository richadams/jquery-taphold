A taphold event for jQuery.

Click/tap and hold for 1s (default) on an element to trigger a taphold event. If you release before the 1s then a normal click event is triggered instead. If you drag outside of the element while holding, then no event is triggered.

Usage:

    $("#element").bind("taphold", function()
    {
        // Actions
    });

    // or

    $("#element").on("taphold", function()
    {
        // Actions
    });

You can combine the event with a click event but just also specifying a click event.

    $("#element").on("taphold", function()
    {
        // Actions for taphold
    })
    .on("click", function()
    {
        // Actions for normal click
    });

Or you can specify the click callback in the `clickHandler` option.

    $("#element").on("taphold",
                     {clickHandler: function() { // Do this on click. }},
                     function() { // Do this on taphold. });

You can change the duration by passing a new value as an option.

    $("#element").on("taphold", {duration: 2000}, function()
    {
        // Actions will trigger after 2s instead of the default of 1s.
    });
