# List of installed packages
installed_pkgs <- installed.packages()

# List of loaded packages
loaded_pkgs <- names(sessionInfo()$loadedOnly)

# Path to your R script
path_to_script <- "path/to/your/script.R"

# Read the lines of the script file
script_lines <- readLines(path_to_script)

# Extract the package names from the library and require functions in the script
library_pkgs <- unique(sub("library\\((.*)\\)", "\\1", grep("library\\(", script_lines, value = TRUE)))
require_pkgs <- unique(sub("require\\((.*)\\)", "\\1", grep("require\\(", script_lines, value = TRUE)))

# Combine the lists of loaded packages, library packages, and require packages
used_pkgs <- unique(c(loaded_pkgs, library_pkgs, require_pkgs))

# Display the list of used packages
print(used_pkgs)
